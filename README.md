# Spatial Statistical Analysis of Rainfall Patterns in Southern Italy

## Overview

This report presents a comprehensive spatial statistical analysis of rainfall data collected across the Southern Italian regions of Calabria and Basilicata. The primary objective is to accurately interpolate rainfall measurements over this geographically diverse area by employing advanced geostatistical techniques that account for spatial dependencies and variations. The analysis aims to assess the most suitable interpolation method within this specific context.

## Key Features & Methodologies

The project systematically explores and applies various spatial modeling techniques:

1.  **Exploratory Data Analysis (EDA):**
    * Non-spatial EDA, including correlation between rainfall and elevation, and normality testing (Shapiro-Wilk).
    * Spatial EDA, incorporating trend analysis (first and second-order polynomial trends) and empirical variogram estimation.
    * Application of Box-Cox transformation for data normalization (optimal λ=0.2).
    * Leave-One-Out Cross-Validation (LOOCV) for model selection, preferring the Exponential variogram model for its simplicity.

2.  **Inverse Distance Weighting (IDW):**
    * Detailed introduction and implementation of the IDW interpolation technique.
    * Methodology for choosing the optimal power parameter `p` using LOOCV to minimize RMSE (optimal p=3).
    * Mapping of interpolated rainfall surfaces and discussion of IDW advantages (simplicity, no distributional assumptions) and limitations (sensitivity to outliers, lack of prediction standard errors).

3.  **Kriging (Classical & Bayesian):**
    * Introduction to the Kriging technique based on the spatial Gaussian mixed model.
    * Maximum Likelihood (ML) Estimation and Prediction, including the use of REML likelihood.
    * Implementation of Classical Kriging for rainfall interpolation, yielding an RMSE of 256.01.
    * **Bayesian Kriging:** Exploration of the Bayesian framework, treating parameters as random quantities and utilizing prior distributions.
    * Comparison of ML Kriging and Bayesian Kriging precision using RMSE (similar results) and Interval Proper Scores, highlighting Bayesian intervals' ability to reflect uncertainty more accurately in data-scarce regions.

## Report Access

The full detailed report, including theoretical background, detailed methodology, figures, and results, is available in PDF format.

[**View Full Report (PDF)**](https://github.com/MatteoVantaggio/Spatial_Statistics_Rainfall_Analysis/blob/main/spatial_statistics_project.pdf) 
