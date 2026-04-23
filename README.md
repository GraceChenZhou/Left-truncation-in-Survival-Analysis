# Tutorial of Left-truncation in Survival Analysis

This vignette provides a step-by-step tutorial on how to analyze competing risks data when both left- truncation and right censoring are present. Specifically, we demonstrate:

- How to estimate the cause-specific cumulative incidence function (CIF) using the cause-specific hazard approach, which gives the probability of a specific event over time in the presence of competing risks.
- How to perform regression modeling of the CIF using the Fine & Gray proportional subdistribution hazards model, which allows you to assess the effect of covariates (e.g., treatment, sex, etc.) on the cumulative incidence in the presence of competing risks.

The main reference is Geskus (2011). The original R function, `crprep`, is included in the R package `mstate`. However, there are some issues with the weight assignment in the original function. After consulting with Dr. Geskus, the bugs were fixed in the function in March 2026. Since this update is not yet available in the `mstate` package, you will need to manually run the updated function provided below to obtain accurate results.


