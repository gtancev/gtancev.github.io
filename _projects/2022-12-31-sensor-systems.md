---
title: 'Low-Cost Gas Sensor Systems and Networks'
subtitle: 'Defining reliable protocols for air quality monitoring in smart cities.'
date: 2022-12-31 00:00:00
description: Low-Cost Gas Sensor Systems and Networks
featured_image: '/images/projects/sensor-systems/1.jpg'
---

![](/images/projects/sensor-systems/1.jpg)

## Summary

High levels of air pollution are harmful to health. Measurement devices are often expensive and therefore sparsely distributed spatially. In some parts of the world, access is even lacking. Furthermore, research has shown that air pollution can vary heavily in small scales, so the personal exposure is often not known. The hope is that such gaps can be filled using low-cost gas sensor systems and networks. However, their reliability is low. The goal of this project was to identify failure modes and design protocols so that trustworthiness can be increased or tracked. I worked on [this project](https://www.aramis.admin.ch/Beteiligte/?ProjectID=44523) as a research scientist at [METAS](https://www.metas.ch/metas/en/home.html) and the results, i.e., published works, became the basis for my doctoral degree.

Firstly, the relocation problem with field calibrated systems was revised and [traced back to lacking representativeness of the calibration data](https://www.mdpi.com/1424-8220/20/21/6198), typically followed by concept drift. With this knowledge, a [compact continuous-flow automaton](https://ieeexplore.ieee.org/abstract/document/9856703) that allows characterizing cross-sensitivities and interferences with environmental factors as well as resolving spatial and temporal relocation problems was developed. It generates orthogonal atmospheres, i.e., gas mixtures at different relative humidities and temperatures, in an efficient manner using fractional factorial designs for the simultaneous calibration of an array of low-cost sensor systems in the laboratory.

 For field calibrated systems, which are heavily affected by concept drift, [machine learning algorithms that monitor the trustworthiness of incoming measurements](https://www.mdpi.com/1424-8220/21/9/3298) were proposed and discussed. Anomalies are detected by estimating the support of the sensor signal distribution and by assessing the position of new signals with respected to this support. Moreover, it is demonstrated how such algorithms might be evaluated with strategies from software validation.
 
Lastly, a theoretical concept for the [stochastic online recalibration of gas sensor networks by means of mobile reference instruments](https://ieeexplore.ieee.org/abstract/document/9690889) was presented. Recently developed gradient update rules such as RMSProp (with and without momentum) are explored. The analysis demonstrates that the reliability of the measurements could be maintained in this manner as sensor aging and concept drift are continuously compensated.

<div class="gallery" data-columns="2">
	<img src="/images/projects/sensor-systems/wf_1.png">
	<img src="/images/projects/sensor-systems/wf_2.png">
	<img src="/images/projects/sensor-systems/wf_3.png">
	<img src="/images/projects/sensor-systems/wf_4.png">
</div>
