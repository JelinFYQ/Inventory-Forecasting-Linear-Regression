# Inventory-Forecasting-Linear-Regression
This repository presents my capstone research on leveraging Machine Learning for Demand Forecasting and Inventory Optimization.
Many companies struggle with inventory forecasting, frequently misjudging stock levels due to outdated methods or unpredictable demand patterns & surges. 
This project aims to use machine learning model with Sales quantity as the target variable to predict the quantity for inventory team to stock up for potential sales. 

# Dataset
The dataset is taken from Kaggle.com
Dataset contains columns such as Date, Store, Product, Category, Region, Inventory Level, Units sold, Units ordered, demand forecast, price, discount, weather condition, holiday/promotion, competitor pricing and seasonality.

# Modeling
# Model 1 - Linear Regression with one variable (Stock Level)
Stock level is the only variable with the highest positive correlation of 0.59 which predicts Sales qty better.
Other variables have near zero correlation with Sales qty, indicating a weak linear relationship.
Evaluation of the Model with R², Train score and R², Test Score of 0.348 and 0.348 respectively. Though the score explains only 34% of the variance in sales qty, it gives the best result compared to other models based on R², Test Score.
This is considered a bad score however that is the best of capability this dataset could do with stock level as the highest correlation variable.

# Model 2 - Random Forest with one variable (Stock Level)
Evaluation of the Model with R², Train score and R², Test Score of 0.353 and 0.342 respectively.
# Model 3 - Linear Regression with three variables (Stock Level, Category and Order Qty)
Evaluation of the Model with R², Train score and R², Test Score of 0.348 and 0.347 respectively.

# Limitations
- Weak linear relationships : Although stock level emerged as the strongest predictor of sales qty, its correlation of 0.59 suggests only moderate relationship
- Excessive categorical features : While categorical variables are valuable, one-hot encoding significantly expands the dataset without improving predictive accuracy
- Limited Influence of External Factors : Variables such as weather and seasonality could impact sales, but the dataset reflects consistent and stable sales patterns, suggesting these features are not strong predictors.

# Recommendations
- Businesses should focus on optimizing stock levels for high selling products and categories
- Maintaining stock level between 50-200 units is ideal based on the sales trend
- Monitor stock level for products with unusual high demand and collaborate with relevant stakeholders to gain insights for accurate sales forecasting
  
# Future Explorations
- The model used was the most fundamental / widely used (LR model). Since performance was not good on linear models, further techniques like non-linear models (XGBoost / Polynomial Regression) could be explored by capturing complex relationships within the data. 
- Time series forecasting model could be explored to predict sales qty based on historical trends, seasonal patterns and cyclical behaviors (if any).
  
