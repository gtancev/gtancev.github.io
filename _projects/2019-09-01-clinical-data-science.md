---
title: 'Clinical Data Science'
subtitle: 'Searching for risk factors of mortality.'
date: 2019-09-01 00:00:00
description: Clinical Data Science
featured_image: '/images/projects/clinical-data-analysis/1.jpg'
---

![](/images/projects/clinical-data-analysis/1.jpg)

## Summary

Various parameters must be considered for **dialysis** intensity dosing in **pediatric patients** suffering from **chronic kidney disease**. It has been observed that certain children die relatively quickly after starting treatment, and one open question is whether there is a subgroup for whom therapy is not yet optimal. I worked on this project as part of [Julia Vogt's research group](https://mds.inf.ethz.ch/team/detail/julia-vogt/) together with clinical scientists at the University Children's Hospital in Basel. Armed with a huge data set of demographic, treatment, and laboratory data, my task was to look for all possible **risk factors** and **biomarkers** using machine learning so that classes of failure modes could be identified. I performed this task with Python using [pandas](https://pandas.pydata.org) for data wrangling, [scikit-learn](https://scikit-learn.org/stable/index.html) for modeling, and [matplotlib](https://matplotlib.org) for visualization.

[The analysis showed that certain variables are good predictors of mortality](https://academic.oup.com/ndt/article/36/3/519/5854486). Some biomarkers were already known from the literature, others were new and required contextualization and careful discussion. Interestingly, one of the most important findings was that the therapy was quite optimal in terms of dosage, as mortality changed most around the recommended levels.[^1]

[^1]: These results were also presented [at a conference](https://www.page-meeting.org/default.asp?abstract=9828).

<div class="gallery" data-columns="3">
	<img src="/images/projects/clinical-data-analysis/feature_importance.png">
	<img src="/images/projects/clinical-data-analysis/pdp_hist_joint.png">
	<img src="/images/projects/clinical-data-analysis/correlations_app.png">
	<img src="/images/projects/clinical-data-analysis/pdp_joint.png">
	<img src="/images/projects/clinical-data-analysis/dr_final_analysis_app.png">
	<img src="/images/projects/clinical-data-analysis/ROC_curve_app.png">
</div>
