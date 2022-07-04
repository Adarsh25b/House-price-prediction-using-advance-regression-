# House-price-prediction-using-advance-regression-
The following challenge is from Kaggle. All the data and descriptions are available at https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques. The training  data consists of 80 features and 1460 training examples to predict the SalePrice of the house. The test data consists of 1459 test examples.

First the training data was analyzed and the categorical and numerical features were known.Then correlation of  different features with the target variable was analyzed and the top 50% correlated features were sent for oultiers removal (if any) as outliers in these features can effect the performance significantly . Boxplots and Regplots were used to visualize the outliers.

The missing values in different features were then identified. All the features with the missing values were imputed accordingly with the mean, mode , None or 0. Numerical features which  were actually categorical were converted to categorical features. Ordinal Encoding was done for Ordinal features and One Hot Encodng for the nominal features. For handling of missing values both training and test data were combined and handled for missing values after separating the target column from the training data.

Skewed features were identified and box cox trasformation was applied. The target variable was also  identified as skewed and logarithm transformation was applied to it.

Feature Scaling was applied on the features.

Various regression model such as Lasso Regression, Linear Regression , RandomForestRegression and GradientBosstingRegression  were applied for th training data. Hyperparameter tuning was done using GridSearchCV with 2 fold cross validation. The model with best parameters was fitted and the score(accuracy) was calculated for different models. The model with highest accuarcy (GradientBosstingRegression-96.78%) was used as the final model to predict using the test  data. The result were submitted for the  evaluation using Root-Mean-Squared-Error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales price to which the model obtained score of 0.13133.

