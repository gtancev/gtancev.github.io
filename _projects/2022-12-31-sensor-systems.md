---
title: 'Low-Cost Gas Sensor Networks'
subtitle: 'Defining protocols for reliable air pollution monitoring.'
date: 2022-12-31 00:00:00
description: Low-Cost Gas Sensor Networks
featured_image: '/images/projects/sensor-systems/1.jpg'
---

![](/images/projects/sensor-systems/1.jpg)

## Summary

[High levels of air pollution are harmful to health](https://doi.org/10.1016/S2542-5196(20)30272-2) and thus need to be monitored. However, measurement devices are generally expensive and therefore sparsely distributed spatially. [Meanwhile, research has shown that air pollution can vary widely on small scales](https://doi.org/10.1021/acs.est.7b00891), so personal exposure at the current coverage in cities is unknown. In some parts of the world there is even a lack of access. The hope is that such gaps can be filled by means of (electrochemical) low-cost gas sensor systems and networks (Fig. 1).

<center>
<figure>
<img src="/images/projects/sensor-systems/low_cost_gas_sensor.jpeg" width="500">
<figcaption><b>Fig. 1:</b> Schema of an electrochemical low-cost gas sensor.</figcaption>
</figure>
</center>

Nonetheless, the low gas sensor price comes at the expense of lower reliability. Cross-sensitivities (i.e., a lack of selectivity), interferences with environmental factors such as temperature and humidity, high unit-to-unit variability, sensor aging, and concept drift are common deficiencies. Typically, these systems are calibrated using field data and machine learning algorithms (e.g., random forests or neural networks) to overcome some of these shortcomings.

Still, the operation of a larger sensor network in a city is very challenging due to the number and frequency of maintenance (i.e., recalibration) required. Although solutions exist with algorithms such as [blind calibration](https://gtancev.github.io/blog/blind-calibration), these only work if certain assumptions are met, [which does not seem to be the case for air pollution monitoring](https://ieeexplore.ieee.org/document/8405565).

The aim of [this project](https://www.aramis.admin.ch/Beteiligte/?ProjectID=44523) was to address the remaining failure modes and design protocols to increase or track the reliability. Also, the question arose as to what extent algorithms are trustworthy at all. I worked on this as a research scientist at [METAS](https://www.metas.ch/metas/en/home.html) and the peer-reviewed publications eventually became the basis for my doctoral degree.

---

### Identifying failure modes of field calibration.

First, the relocation problem with field calibrated systems was revised and [traced back to lacking representativeness of the calibration data](https://www.mdpi.com/1424-8220/20/21/6198), typically followed by concept drift. In other words, the quality of the data decreases when the devices are moved to a different location, but it can also decrease over time after it has been in the same location. This work replicated field calibrations and examined the resulting models and the data used with techniques from data science. The main finding was that the cause was the lack of representativeness of the calibration data and the strong correlations between the measured variables. If the relationships between the variables change, the calibration model also becomes invalid. It was concluded that this problem could be solved by using [orthogonal experimental designs](https://gtancev.github.io/blog/design-of-experiments).

<center>
<figure>
<img src="/images/projects/sensor-systems/wf_1.png" width="800">
<figcaption><b>Fig. 2:</b> Workflow of the data analysis.</figcaption>
</figure>
</center>

---

### Developing a robust calibration method for the laboratory.

With this knowledge, a [compact continuous-flow automaton](https://ieeexplore.ieee.org/abstract/document/9856703) that allows characterizing cross-sensitivities and interferences with environmental factors as well as resolving spatial and temporal relocation problems was developed. It generates orthogonal atmospheres, i.e., gas mixtures at different relative humidities and temperatures, in an efficient manner using fractional factorial designs for the simultaneous calibration of an array of low-cost sensor systems in the laboratory. Such devices can then serve as mobile references (e.g., on top of buses or trams) to recalibrate other low-cost devices.

<center>
<figure>
<img src="/images/projects/sensor-systems/wf_2.png" width="800">
<figcaption><b>Fig. 3:</b> Specifications of the laboratory calibration.</figcaption>
</figure>
</center>

---

### Using predictive maintanance.

For field calibrated systems, which are heavily affected by concept drift, [machine learning algorithms that monitor the trustworthiness of incoming measurements](https://www.mdpi.com/1424-8220/21/9/3298) were proposed and discussed. [Anomalies are detected by estimating the support of the sensor signal distribution and by assessing the position of new signals with respected to this support](https://gtancev.github.io/blog/robust-covariance). Moreover, it was demonstrated how such algorithms might be evaluated with strategies from software validation (i.e., evaluation in "virtual evironments" via numerical simulations based on finite difference equations).

<center>
<figure>
<img src="/images/projects/sensor-systems/wf_3.png" width="800">
<figcaption><b>Fig. 4:</b> Usage of predictive maintenance.</figcaption>
</figure>
</center>

---

### Designing a field recalibration method.

Finally, a theoretical concept for the [stochastic online recalibration](https://gtancev.github.io/blog/stochastic-calibration) of gas sensor networks by means of mobile reference instruments was presented. In essence, measured values would be compared during encounters and the calibration models would be adjusted by means of stochastic gradient updates. Recently developed gradient update rules such as RMSProp (with and without momentum) were explored. The algorithms and their design parameters were evaluated using Monte Carlo simulations. [The analysis suggested that the reliability of the measurements could be maintained in this manner as sensor aging and concept drift are continuously compensated](https://ieeexplore.ieee.org/abstract/document/9690889).

<center>
<figure>
<img src="/images/projects/sensor-systems/wf_4.png" width="800">
<figcaption><b>Fig. 5:</b> Stochastic online calibration with mobile references.</figcaption>
</figure>
</center>
