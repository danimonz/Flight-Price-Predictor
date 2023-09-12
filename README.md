# Flight Price Predictor
I undertook a Flight Price Predictor project, where I began by meticulously cleaning and preparing the South-Asian Flight data, transforming it into both continuous and categorical variables for analysis. To optimize our model's performance, I employed the ExtraTreesRegressor from scikit-learn to rank the importance of 25 available features, subsequently dropping those deemed unnecessary. Additionally, I rigorously checked for multicollinearity in the dataset using the Variance Inflation Factor (VIF) method.

To deliver accurate predictions, I trained a random regressor model using a dedicated test set and meticulously evaluated its performance using key error metrics such as mean absolute error (MAE) and mean squared error (MSE).

#Data
Dataset is a collection of flight observations from several airlines taken place in Southern Asia in the year 2019.
Data came from https://www.kaggle.com/datasets/nikhilmittal/flight-fare-prediction-mh.

![Figure5FeatureImportance](https://github.com/danimonz/Flight-Price-Predictor/assets/56010144/6355dd64-5717-48f8-a15d-71c2244e2d60)
- The plot lists the features from lowest to highest by rank of importance. We can see features that observe the total number of stops, dates, and times of a flight that are ranked the highest and have the most influence. The airline or destination of a flight seems to have the least importance.

![Figure6VIF](https://github.com/danimonz/Flight-Price-Predictor/assets/56010144/3fa478d4-abdb-4e91-af2b-ff733c132570)
- The remaining features and their VIF values are shown after the removal of features with high VIF values and low importance. Although "journey\textunderscore month" has a high VIF value, we know it also has high importance so we sacrifice model performance to avoid overfitting.

![Figure7FeatureLinear](https://github.com/danimonz/Flight-Price-Predictor/assets/56010144/eba17e17-7a58-4270-aaee-c9ed60f351ae)
- The plot lists the features from lowest to highest by rank of importance for a linear model. Unlike the feature importance ranking for the random trees regressor model, we can see that the airlines the flights belong to are ranked very high while date features such as "journey_month" and "journey_day" are ranked very poorly.

![Figure8RandomForest](https://github.com/danimonz/Flight-Price-Predictor/assets/56010144/fa0c5856-c6e8-4f5d-b8ad-8dd8db0de9e5)
- The plot shows a fairly decent linear relationship in the data points. The clump of data is a bit more spread out and more closely fits the reference line than linear regression. This is due to the better selection of features the model used.

![Figure9LinearRegression](https://github.com/danimonz/Flight-Price-Predictor/assets/56010144/d9e9089b-200a-443c-8955-b0ca823496dd)
-






