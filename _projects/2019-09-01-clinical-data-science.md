---
title: 'Clinical Data Science'
subtitle: 'Searching for risk factors of mortality.'
date: 2019-09-01 00:00:00
description: Clinical Data Science
featured_image: '/images/projects/clinical-data-analysis/1.jpg'
---

![](/images/projects/clinical-data-analysis/1.jpg)

## Summary

### Motivation

In this project, conducted in the research group of Julia Vogt at the University Hospital Basel, I worked on analysing clinical data from children with end-stage renal disease receiving chronic haemodialysis. The goal was to use data-science methods to identify predictors of mortality and assess their relevance using statistical and machine-learning approaches.

The work is directly linked to the publication [Identifying key predictors of mortality in young patients on chronic haemodialysis – a machine learning approach (NDT, 2021)](https://academic.oup.com/ndt/article/36/3/519/5854486).[^1]

### My contribution

I was responsible for the full data-science pipeline:

- Data preparation and feature engineering
	Cleaning, structuring, and enhancing the clinical database (demographics, labs, treatment parameters), including derivation of additional features.
- Exploratory data analysis
	Examination of potential risk factors, initial hypothesis generation, and visual pattern analysis.
- Machine-learning modelling
	Application of modern ML methods (e.g., Random Forests, Gradient Boosting) to identify key predictors of mortality and quantify their importance robustly.
- Interpretation in clinical context
	Extraction of the most relevant factors (e.g., albumin, inflammatory markers, dialysis parameters) and contextualisation of results together with clinical collaborators.

### Outcome

The analysis confirmed established risk markers and highlighted additional variables that had been underappreciated. Overall, the ML workflow helped refine clinical risk assessment and identify vulnerable patient subgroups more objectively.

This project illustrates how modern data-science methods can be applied in sensitive clinical environments — combining rigorous modelling, interpretability, and interdisciplinary collaboration between clinical medicine and machine learning.

[^1]: These results were also presented [at a conference](https://www.page-meeting.org/default.asp?abstract=9828).

<div class="gallery" data-columns="3">
	<img src="/images/projects/clinical-data-analysis/feature_importance.png">
	<img src="/images/projects/clinical-data-analysis/pdp_hist_joint.png">
	<img src="/images/projects/clinical-data-analysis/correlations_app.png">
	<img src="/images/projects/clinical-data-analysis/pdp_joint.png">
	<img src="/images/projects/clinical-data-analysis/dr_final_analysis_app.png">
	<img src="/images/projects/clinical-data-analysis/ROC_curve_app.png">
</div>
