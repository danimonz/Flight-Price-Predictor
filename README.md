# Flight Price Predictor
I undertook a Flight Price Predictor project, where I began by meticulously cleaning and preparing the South-Asian Flight data, transforming it into both continuous and categorical variables for analysis. To optimize our model's performance, I employed the ExtraTreesRegressor from scikit-learn to rank the importance of 25 available features, subsequently dropping those deemed unnecessary. Additionally, I rigorously checked for multicollinearity in the dataset using the Variance Inflation Factor (VIF) method.

To deliver accurate predictions, I trained a random regressor model using a dedicated test set and meticulously evaluated its performance using key error metrics such as mean absolute error (MAE) and mean squared error (MSE).

#Data
Dataset is a collection of flight observations from several airlines taken place in Southern Asia in the year 2019.
Data came from https://www.kaggle.com/datasets/nikhilmittal/flight-fare-prediction-mh.
