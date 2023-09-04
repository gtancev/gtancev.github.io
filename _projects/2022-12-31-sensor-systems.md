---
title: 'Low-Cost Gas Sensor Systems and Networks'
subtitle: 'Defining reliable protocols for air quality monitoring in smart cities.'
date: 2022-12-31 00:00:00
description: Low-Cost Gas Sensor Systems and Networks
featured_image: '/images/projects/sensor-systems/1.jpg'
---

![](/images/projects/sensor-systems/1.jpg)

## Summary

[High levels of air pollution are harmful to health](https://doi.org/10.1016/S2542-5196(20)30272-2). Measurement devices are often expensive and therefore sparsely distributed spatially. In some parts of the world, access is even lacking. Furthermore, research has shown that air pollution can vary heavily in small scales, so the personal exposure is often unknown. The hope is that such gaps can be filled by means of low-cost gas sensor systems and networks. However, their reliability is low. The goal of this project was to identify failure modes and design protocols so that trustworthiness can be increased or tracked. I worked on [this project](https://www.aramis.admin.ch/Beteiligte/?ProjectID=44523) as a research scientist at [METAS](https://www.metas.ch/metas/en/home.html) and the peer-reviewed publications became the basis for my doctoral degree in the end.

---

Firstly, the relocation problem with field calibrated systems was revised and [traced back to lacking representativeness of the calibration data](https://www.mdpi.com/1424-8220/20/21/6198), typically followed by concept drift.

<img src="/images/projects/sensor-systems/wf_1.png" width="800">

---

With this knowledge, a [compact continuous-flow automaton](https://ieeexplore.ieee.org/abstract/document/9856703) that allows characterizing cross-sensitivities and interferences with environmental factors as well as resolving spatial and temporal relocation problems was developed. It generates orthogonal atmospheres, i.e., gas mixtures at different relative humidities and temperatures, in an efficient manner using fractional factorial designs for the simultaneous calibration of an array of low-cost sensor systems in the laboratory.

<img src="/images/projects/sensor-systems/wf_2.png" width="800">

---

For field calibrated systems, which are heavily affected by concept drift, [machine learning algorithms that monitor the trustworthiness of incoming measurements](https://www.mdpi.com/1424-8220/21/9/3298) were proposed and discussed. Anomalies are detected by estimating the support of the sensor signal distribution and by assessing the position of new signals with respected to this support. Moreover, it is demonstrated how such algorithms might be evaluated with strategies from software validation.

 <img src="/images/projects/sensor-systems/wf_3.png" width="800">

---

Lastly, a theoretical concept for the [stochastic online recalibration](https://gtancev.github.io/blog/stochastic-calibration) of gas sensor networks by means of mobile reference instruments was presented. Recently developed gradient update rules such as RMSProp (with and without momentum) are explored. [The analysis suggested that the reliability of the measurements could be maintained in this manner as sensor aging and concept drift are continuously compensated](https://ieeexplore.ieee.org/abstract/document/9690889).

<img src="/images/projects/sensor-systems/wf_4.png" width="800">
