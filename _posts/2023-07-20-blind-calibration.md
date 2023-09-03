---
title: 'Blind Calibration'
date: 2023-07-20 00:00:00
description: An algorithm that keeps your sensor networks calibrated.
featured_image: '/images/demo/demo-square.jpg'
---

![](/images/demo/demo-landscape.jpg)

## Introduction

Wireless sensor networks have emerged as a technology that enables the monitoring and control of processes in manufacturing plants or smart cities. In the case of air quality monitoring in smart cities, for example, particularly polluted places could be identified in real-time and citizens protected from the effects of air pollution. These networks consist of many distributed sensor nodes that collect data and transmit them to a central place where they can be processed.

Such measurement systems, however, place new demands on calibration, e.g., in terms of scale and frequency. More precisely, these countless sensors are often of inferior quality and therefore need calibration more often. Manually calibrating each node or collecting all nodes and bringing them to a laboratory (for calibration) would be too tedious, if not impossible, and would also result in downtime and missing data. Still, calibrations are necessary because they make measurements comparable in space and time. If sensors drift, their measured values do not correspond to the truth. As a result, decisions based on such data will be unreasonable.

How to keep sensor networks calibrated has therefore been the subject of research, giving rise to so-called [blind calibration algorithms](https://link.springer.com/chapter/10.1007/978-0-387-68845-9_1) (among other types of automated calibration techniques), which aim at improving the data quality of measurements of the sensors and delay (or even omit) expensive manual calibrations. Simply put, they use an initial calibration as a reference; the key idea is to exploit correlations between sensor signals, allowing to compute new calibration coefficients using techniques from linear algebra and mathematical optimization. This article explains the theory behind such algorithms and demonstrates their potential and limitations with a practical example.

## Theoretical Background

The starting point is a sensor network consisting of n nodes, each sensing a certain process. At time t, the individual measurements are collected as in a vector y = [y₁, …, yₙ]. If the individual sensors “see the same thing”, their signals will be correlated to a large degree. Such correlation can happen if the phenomenon to be measured behaves similarly at different locations or all sensors are at the same location measuring the same or different processes that are coupled. As a consequence, the collection of measurements will lie in a subspace of dimensionality r < n. Although the sensors will be calibrated initially, gain α ∈ ℝⁿ and offset β ∈ ℝⁿ drift (shown in Fig. 1) will make recalibration necessary, that is,

x = Yα + β,

with Y = diag(y).

If we learn the projection matrix 𝐏 of dimensionality n - r associated with the signal nullspace (i.e., the orthogonal complement to the signal subspace 𝒮), we can try to estimate the correct gain and offset coefficients. The idea is that the true signals should remain in the signal subspace 𝒮 at all times, that is,

𝐏x = 𝐏(𝐘α + β) = 0.

The part of the drift in 𝒮, however, cannot be recovered, so it must be assumed that the average signal has a zero mean. Note that too much noise destroys existing correlations. Another important prerequisite is that the basis is robust (the correlations have to persistent). This projection matrix 𝐏 can easily be found by collecting measurements in an initial phase (in which the sensors have no drift at all) and by performing a principal component analysis.

Then, if we collect k snapshots,

𝐏(𝐘ᵢα + β) = 0 with i = {1, …, k},

we can use them to compute the calibration factors (almost) blindly. The formula above holds for any Y, in particular also for the average Y̅. From this observation, we can conclude that

β̂ = −Y̅α.

Inserting this expression for β, we obtain

𝐏(𝐘ᵢ−Y̅)α = 0, for i = {1, …, k}.

The individual snapshots 𝐏(𝐘ᵢ−Y̅) can be stacked in a matrix 𝐂. Because the observations are noise, we minimize a squared loss with respect to the gain vector α to obtain

α̂ = arg min αᵀ 𝐂ᵀ 𝐂 α

with the constraint that α₁ = αₜᵣᵤₑ, that is, we need to know at least one gain factor, but it does not matter which one. Alternatively, we could also fix any of the gains to 1, and the other gains would be relative to this so-called global gain factor. Such a constraint can be interpreted physically to mean that all sensors are calibrated to the gain characteristics of sensor 1. The raison d’être for the constraint is that the solution will be α̂ = 0 without it, which is not what we want.

One interesting question is how many snapshots to collect, i.e., what value to choose for k. For the gains, it holds that k ≥ ⌈(n - 1)/(n - r)⌉. Since the offsets are then computed from an average, more snapshots will generally lead to a more precise estimate.

## Methods

