A statistical analysis of customer satisfaction survey data from the Swiss Link market research institute, covering 1,033 respondents across 18 questions scored on a 1–10 scale. The goal is to identify the main drivers of overall satisfaction (g27a) and to assess whether the questionnaire's dimensionality can be meaningfully reduced.
The workflow, implemented entirely in R, includes:

Missing data treatment — diagnosed non-random missingness via TestMCARNormality and paired t-tests, then applied multiple imputation (MICE with Predictive Mean Matching).
Regression modeling — fitted OLS, identified influential observations through Cook's distances, and refit using MM-estimator robust regression to handle outliers; the full-variable model achieved adjusted R² ≈ 0.76.
Dimensionality reduction — compared 2- and 3-factor models (varimax rotation), selecting the 2-factor solution, and validated structure with hierarchical clustering (Ward's method).

The analysis identifies food taste, general service quality, friendliness, and atmosphere as the strongest determinants of satisfaction, while parking and public-transport access show negligible effect. The 18 questions collapse naturally into three interpretable clusters: human service quality, physical/environmental quality, and food quality.
Tools: R (tidyverse, MICE, robustbase, psych, corrplot, ggridges).
