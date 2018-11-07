
# Ryan Stewart's Capstone Project - The Value of Health

The purpose of this project was to explore the relationship between health metrics and per capita income.
Health data was gathered from the CDC's "500 Cities" dataset, and income data for US counties was gathered from wikipedia.

## Contents
Data cleaning work can be found in the cleaning_health_data, dc_data, and formatting_income_data notebooks.
Health data was aggregated to the county level and combined with income data by using 5-digit fips codes.
For more detail on the data cleaning process for this dataset, check out my article in Towards Data Science here: https://towardsdatascience.com/breaking-down-the-cdcs-500-cities-health-metrics-data-set-code-included-625ed534088e

Predictive modeling can be found in the modeling_and_exploration notebook:
Modeling techniques used included Linear Regression, neural networks, XGBoost, GradientBoost, Lasso, and RandomForest.
While XGBoost had the best performance, I focused on the Linear Regression model because its performance was not far off
of XGBoost, and linear regression allowed me to look closely at the impact of specific health metrics on the model.

## Findings and Notes
I found that health data from "500 Cities" can be used to predict per capita income within less than $3,500 on average.
Specific recommendations on areas for Washington DC to focus on improving health(i.e. Binge Drinking and Smoking), along with 
associated monetary benefits are discussed in the powerpoint presentation.

Some limitations of this project include that census-tract level income data were not available, so health data had to be
aggregated to the county level in order to incorporate income. Furthermore, because I had to aggregate health data, specific
recommendations can only be made at the county level. (DC is included as a county because of its status as a District).
Next steps to improve the usefulness of this model are to find or gather census-level income data to improve the precision of my analysis and recommendations.
