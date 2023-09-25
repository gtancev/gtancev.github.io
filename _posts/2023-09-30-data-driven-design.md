---
title: 'Data-Driven Chemical Process Design'
date: 2040-09-01 00:00:00
description: Data-Driven Chemical Process Design
featured_image: '/images/posts/data-driven-design/1.jpg'
---

![](/images/posts/data-driven-design/1.jpg)

## Problem Definition

Process development and design are labor-intensive, costly endeavors. By reaching good process designs faster, a great deal can be saved. Established chemical companies have accumulated a tremendous amount of knowledge about process development. This experience is usually passed on from incumbent scientists to the next generation. With demographic shifts, they are slowly dropping away, leading to a reduction of the available workforce (i.e., increase in labor expenses) and a loss of knowledge.

The rules and heuristics that are applied in this field are latent in the design choices made. This is typically triggered by the molecular structures inducing microscopic properties. A molecule without functional groups, for example, only dissolves in apolar solvents. Therefore, only such solvents can be used for its homogeneous reaction. This implicitly results in the rule that "similar things dissolve in similar things." In the appropriate process documentation, this would be recovered.

Thinking this further, similar transformations should induce similar process designs. After all, such rules are also applied by experts when they solve problems. If one succeeded in adequately extracting and representing this knowledge from data, then one could search for design proposals as a function of compounds or chemical transformations (Fig. 1).

<center>
<figure>
<img src="/images/posts/data-driven-design/proposal.png" width="600">
<figcaption><b>Fig. 1:</b> Workflow.</figcaption>
</figure>
</center>

This approach has similarities to previous expert systems, with design and planning already applied. The difference between now and the past is that knowledge no longer has to be taken from the experts first, but is learned from data.

## Strategy

First, the question arises to what extent all work has been carefully documented. In the beginning, one would have to make an inventory in any case and the available information needs to be gathered. Typically, this represents the greater part of the task. Once this knowledge is available in databases, it can be activated. If insufficient data are available, the situation is hopeless.

However, the fact that processes are hierarchical has been concealed so far. The chances of success are better if individual steps are focused on. Designs of certain manufacturing stages are likely to be more promising than others. In addition, there is the question of how exactly to represent a process design. Which data must be included for a good basic design? What kind of design prototypes would make the most sense? Most likely, such information must be extracted and transformed from different sources first to load it into a target database. 

The result would be a kind of hash table in which molecular structures serve as keys and the designs represent entries. In the simplest form, the input/output compounds (or even macroscopic structures) could simply be compared. Two molecules with similar structures should require similar transformations, i.e., designs, compared to less similar ones. To compare the similarity between compounds, one can use, for instance, graph kernels. A graph kernel is a function that captures the inner product between two graphs. Furthermore, new kernels can be created from existing ones through kernel composition. Algorithms such as support vector machines or Gaussian processes rely on them for design classification.

However, there is no guarantee that the proposed designs will be any good. On the one hand, it may be that new components deviate too firmly from existing ones. On the other hand, the granularity of the designs may not appropriate (i.e., information might be missing or incorrect). In this sense, users must also not blindly trust the system. This implies that while the amount of work might be less in some cases, it would not be completely eliminated.
