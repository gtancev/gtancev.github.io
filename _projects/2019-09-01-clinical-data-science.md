---
title: 'Clinical Data Science'
subtitle: 'Searching for risk factors of mortality.'
date: 2019-09-01 00:00:00
description: Clinical Data Science
featured_image: '/images/projects/clinical-data-analysis/1.jpg'
---

![](/images/projects/clinical-data-analysis/1.jpg)

## Summary

I worked on this project as part of [Julia Vogt's research group](https://mds.inf.ethz.ch/team/detail/julia-vogt/) together with clinical scientists at the University Children's Hospital in Basel.
Various parameters must be considered for dialysis intensity dosing in pediatric patients suffering from chronic kidney disease. What has been observed before is that certain children die relatively quickly after starting their treatment, and one important question was if there was a subpopulation for which the therapy was not yet optimal. Armed with a huge data set of demographic, treatment, and laboratory data, my task was to look for all possible risk factors and biomarkers such that classes of failure modes can be identified.

[The analysis showed that certain variables are good predictors of mortality](https://academic.oup.com/ndt/article/36/3/519/5854486). Some biomarkers were already known from the literature, others were new and required contextualization and careful discussion. Interestingly, one of the main findings was that the therapy was quite optimal in terms of dosage, since the mortality changed the most around recommended values.

<div class="gallery" data-columns="3">
	<img src="/images/projects/clinical-data-analysis/feature_importance.png">
	<img src="/images/projects/clinical-data-analysis/pdp_hist_joint.png">
	<img src="/images/projects/clinical-data-analysis/pdp_joint.png">
	<img src="/images/projects/clinical-data-analysis/dr_final_analysis_app.png">
	<img src="/images/projects/clinical-data-analysis/correlations_app.png">
	<img src="/images/projects/clinical-data-analysis/ROC_curve_app.png">
</div>
