Longitudinal Lipidomics Analysis of Left Ventricular Mass and Hypertrophy
Overview

This project involves the analysis of lipidomics data to identify associations between lipid species and left ventricular mass (LV Mass) and left ventricular hypertrophy (LVH) in a longitudinal cohort study. The analysis focuses on two datasets from American Indian participants collected over a follow-up period of approximately 5 years. The study aims to understand how changes in individual lipid species relate to changes in LV mass index (LVMI) and to evaluate the potential role of these lipids as biomarkers for cardiovascular health.

Datasets

data4: Contains data from the first wave of examination (P4). This dataset is used for the cross-sectional analysis of LV Mass Index (LVMI).

data5: Contains data from the second wave of examination (P5). This dataset is used for the follow-up cross-sectional analysis of LVMI.
Both datasets include baseline and follow-up measurements of lipids, demographic variables, and cardiovascular health indicators.

Key Variables

Lipid Species: 1,542 lipid species measured using LC-MS.
LVMI: Left ventricular mass index, the primary outcome measure.
Covariates: Age, sex, BMI, LDL cholesterol, systolic blood pressure, smoking status, diabetes status, and lipid-lowering medication use.
Analysis Pipeline

Step 1: Data Preprocessing
The code begins by loading the datasets (data4 and data5) and performing data cleaning, including filtering for missing values.
Covariates are standardized, and categorical variables are set to appropriate reference levels for analysis.

Step 2: Cross-Sectional Analysis using Generalized Estimating Equations (GEE)
The analysis uses GEE models to examine the cross-sectional associations between individual lipid species and LVMI in both datasets.
Covariates such as age, sex, BMI, and other clinical factors are included in the models to adjust for potential confounders.
Results are stored for each lipid species, including estimates, standard errors, odds ratios, and confidence intervals.

Step 3: Meta-Analysis
Results from the cross-sectional analyses of both datasets are combined using fixed-effects meta-analysis (using the metafor package).
The meta-analysis calculates pooled estimates and assesses heterogeneity between the two datasets.

Step 4: Multiple Testing Correction
The q-values are calculated using the qvalue package to adjust for multiple testing and control the false discovery rate (FDR).
Output
The results for individual datasets are saved in CSV files for further interpretation and visualization.
Meta-analysis results provide a comprehensive view of how lipid species are associated with changes in LVMI across both time points.
