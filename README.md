
# The Value of Health

Notebooks:
1. Cleaning_Combine_Health_And_Income_Data.ipynb
2. Data_Standardization_And_Modeling.ipynb

The purpose of this project was to explore the relationship between health metrics and per capita income.
Health data was gathered from the CDC's "500 Cities" dataset, and income data for US counties was gathered from wikipedia.

Multiple machine learning models were built, and while some were able to slightly outperform the baseline, none provided strong predictive capabilities given the limited data after aggregation.  GridSearch with a RandomForestRegressor tended to provide the best results, and produced a significant reduction in MSE vs the baseline as well as a fairly high R2 score.

While no significant results were identified, this project serves as a starting point.  Sourcing better data will likely lead to stronger predictive capabilities.

## Contents
Health data was combined with income data by tagging cities and lat/long coordinates with zip codes and joining the health and income data on the zipcode.
For more detail on the data cleaning process for the 500 Cities health dataset, check out my article in Towards Data Science here: https://towardsdatascience.com/breaking-down-the-cdcs-500-cities-health-metrics-data-set-code-included-625ed534088e

Data cleaning work can be found in the Cleaning_Combine_Health_And_Income_Data notebook; however, I have also included the final csv outputs of those notebooks in the sourcedata/ and processeddata/ folders for convenience.


Predictive modeling can be found in the Data_Standardization_And_Modeling notebook:
Modeling techniques used included Linear Regression, neural networks, XGBoost, GradientBoost, Lasso, and RandomForest.
Random forest and linear regression were kept in the notebook for demonstration purposes.


## Findings and Notes
Some limitations of this project include that census-tract level income data were not available. As a result, asumptions had to be made, specifically that city/county level income data would be a close-enough approximation of income at the zip code level. A significant portion of data was lost due to the inability to tag it with a specific zip code or due to a lack of income data for that zip code.

The RandomForestRegressor showed the strongest performance when compared to baseline.

Next steps are to find or gather census-level income data to improve the precision of my analysis and recommendations.
