
# The Value of Health

The purpose of this project was to explore the relationship between health metrics and per capita income.
Health data was gathered from the CDC's "500 Cities" dataset, and income data for US counties was gathered from wikipedia.

Multiple machine learning models were built, and while some were able to slightly outperform the baseline, none provided strong predictive capabilities given the limited data after aggregation.  GridSearch with a RandomForestRegressor tended to provide the best (but not significant) results.

While no significant results were identified, this project serves as a starting point.  Sourcing better data will likely lead to stronger predictive capabilities.

## Contents
Data cleaning work can be found in the cleaning_health_data, dc_data, and formatting_income_data notebooks.
Health data was aggregated to the county level and combined with income data by using 5-digit fips codes.
For more detail on the data cleaning process for this dataset, check out my article in Towards Data Science here: https://towardsdatascience.com/breaking-down-the-cdcs-500-cities-health-metrics-data-set-code-included-625ed534088e

Data cleaning work can be found in notebooks 1-3; however, I have also included the final outputs of those
notebooks in the datasets/ folder for convenience.

Predictive modeling can be found in the 4_data_standardization_and_modeling notebook:
Modeling techniques tested included Linear Regression, neural networks, XGBoost, GradientBoost, Lasso, and RandomForest.
Most models have been removed from the notebook, but I have left RandomForest with a Gridsearch and Linear Regression in as they showed the best predictive capability on the limited data.

## Findings and Notes
Some limitations of this project include that census-tract level income data were not available, so health data had to be
aggregated to the county level in order to incorporate income. Furthermore, because I had to aggregate health data, specific
recommendations can only be made at the county level. (DC is included as a county because of its status as a District).

Due to the data limitions noted above, health data could not be reliably used to predict income levels; however, it is possible that more comprehensive data would produce stronger predictions.

Next steps  are to find or gather census-level income data to improve the precision of my analysis and recommendations.
