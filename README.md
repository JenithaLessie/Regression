Project Overview

Our client, a grocery retailer, hired a market research consultancy to append market level customer loyalty information to the database. However, only around 50% of the client's customer base could be tagged, thus the other half did not have this information present.

The overall aim of this work is to accurately predict the loyalty score for those customers who could not be tagged, enabling the client a clear understanding of true customer loyalty, regardless of total spend volume - and allowing for more accurate and relevant customer tracking, targeting, and comms.

To achieve this, I looked to build out a predictive model that will find relationships between customer metrics and loyalty score for those customers who were tagged, and use this to predict the loyalty score metric for those who were not.

![image](https://github.com/user-attachments/assets/d7f71caa-3294-45f2-8462-2d19387b8b14)

Actions
Firstly, I needed to compile the necessary data from tables in the database, gathering key customer metrics that may help predict loyalty score, appending on the dependent variable, and separating out those who did and did not have this dependent variable present.

As I am predicting a numeric output, I tested three regression modelling approaches, namely:

Linear Regression, 
Decision Tree, 
Random Forest


Results
Testing found that the Random Forest had the highest predictive accuracy.


**Metric 1: Adjusted R-Squared (Test Set)**
Random Forest = 0.955, 
Decision Tree = 0.886, 
Linear Regression = 0.754

**Metric 2: R-Squared (K-Fold Cross Validation, k = 4)**
Random Forest = 0.925, 
Decision Tree = 0.871, 
Linear Regression = 0.853


As the most important outcome for this project was predictive accuracy, rather than explicitly understanding weighted drivers of prediction, I chose the Random Forest as the model to use for making predictions on the customers who were missing the loyalty score metric.


Growth/Next Steps
While predictive accuracy was relatively high - other modelling approaches could be tested, especially those somewhat similar to Random Forest, for example XGBoost, LightGBM to see if even more accuracy could be gained.

From a data point of view, further variables could be collected, and further feature engineering could be undertaken to ensure that I have as much useful information available for predicting customer loyalty.
