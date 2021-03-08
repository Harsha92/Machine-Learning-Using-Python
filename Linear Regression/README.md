## Introduction to Linear Regression

__Linear regression__ is a _basic_ and _commonly_ used type of __predictive analysis__.  The overall idea of regression is to examine two things: 
- Does a set of __predictor variables__ do a good job in predicting an __outcome__ (dependent) variable?  
- Which variables in particular are __significant predictors__ of the outcome variable, and in what way they do __impact__ the outcome variable?  

These regression estimates are used to explain the __relationship between one dependent variable and one or more independent variables__.  The simplest form of the regression equation with one dependent and one independent variable is defined by the formula :<br/>
𝑦=𝛽0+𝛽1𝑥

[![Linear Regression](http://www.sthda.com/english/sthda-upload/images/machine-learning-essentials/linear-regression.png "Linear Regression")](http://www.sthda.com/english/sthda-upload/images/machine-learning-essentials/linear-regression.png "Linear Regression")

What does each term represent?
- y is the response
- x is the feature
- 𝛽0 is the intercept
- 𝛽1 is the coefficient for x


Three major uses for __regression analysis__ are: 
- determining the __strength__ of predictors,
    - Typical questions are what is the strength of __relationship__ between _dose and effect_, _sales and marketing spending_, or _age and income_.
- __forecasting__ an effect, and
    - how much __additional sales income__ do I get for each additional $1000 spent on marketing?
- __trend__ forecasting.
    - what will the __price of house__ be in _6 months_?

### Linear Regression Equation with Errors in consideration
While taking errors into consideration the equation of linear regression is: 
[![](https://miro.medium.com/max/875/1*k2bLmeYIG7z7dCyxADedhQ.png)](https://miro.medium.com/max/875/1*k2bLmeYIG7z7dCyxADedhQ.png)

Generally speaking, coefficients are estimated using the **least squares criterion**, which means we are find the line (mathematically) which minimizes the **sum of squared residuals** (or "sum of squared errors"):


## Model evaluation 

__Error__ is the _deviation_ of the values _predicted_ by the model with the _true_ values.<br/>
For example, if a model predicts that the price of apple is Rs75/kg, but the actual price of apple is Rs100/kg, then the error in prediction will be Rs25/kg.<br/>
Below are the types of error we will be calculating for our _linear regression model_:
- Mean Absolute Error
- Mean Squared Error
- Root Mean Squared Error

### Model Evaluation using __metrics.__
__Mean Absolute Error__ (MAE) is the mean of the absolute value of the errors:
1/𝑛∑𝑖=1𝑛|𝑦𝑖−𝑦̂ 𝑖|

__Mean Squared Error__ (MSE) is the mean of the squared errors:
1/𝑛∑𝑖=1𝑛(𝑦𝑖−𝑦̂ 𝑖)2

__Root Mean Squared Error__ (RMSE) is the square root of the mean of the squared errors:

(1/𝑛∑𝑖=1𝑛(𝑦𝑖−𝑦̂ 𝑖)2) ** 0.5

### Model Evaluation using Rsquared value.

- There is one more method to evaluate linear regression model and that is by using the __Rsquared__ value.<br/>
- R-squared is the **proportion of variance explained**, meaning the proportion of variance in the observed data that is explained by the model, or the reduction in error over the **null model**. (The null model just predicts the mean of the observed response, and thus it has an intercept and no slope.)

- R-squared is between 0 and 1, and higher is better because it means that more variance is explained by the model. But there is one shortcoming of Rsquare method and that is **R-squared will always increase as you add more features to the model**, even if they are unrelated to the response. Thus, selecting the model with the highest R-squared is not a reliable approach for choosing the best linear model.

There is alternative to R-squared called **adjusted R-squared** that penalizes model complexity (to control for overfitting).


## Assumptions of Linear Regression
There are 5 basic assumptions of Linear Regression Algorithm:

### 1. Linear Relationship between the features and target:

According to this assumption there is linear relationship between the features and target.Linear regression captures only linear relationship.This can be validated by plotting a scatter plot between the features and the target.

### 2.Little or no Multicollinearity between the features:

Multicollinearity is a state of very high inter-correlations or inter-associations among the independent variables.It is therefore a type of disturbance in the data if present weakens the statistical power of the regression model.Pair plots and heatmaps(correlation matrix) can be used for identifying highly correlated features.

Why removing highly correlated features is important?
The interpretation of a regression coefficient is that it represents the mean change in the target for each unit change in an feature when you hold all of the other features constant. However, when features are correlated, changes in one feature in turn shifts another feature/features. The stronger the correlation, the more difficult it is to change one feature without changing another. It becomes difficult for the model to estimate the relationship between each feature and the target independently because the features tend to change in unison.

How multicollinearity can be treated?
If we have 2 features which are highly correlated we can drop one feature or combine the 2 features to form a new feature,which can further be used for prediction.

### 3.Homoscedasticity Assumption:

Homoscedasticity describes a situation in which the error term (that is, the “noise” or random disturbance in the relationship between the features and the target) is the same across all values of the independent variables.A scatter plot of residual values vs predicted values is a goodway to check for homoscedasticity.There should be no clear pattern in the distribution and if there is a specific pattern,the data is heteroscedastic.

### 4.Normal distribution of error terms:

The fourth assumption is that the error(residuals) follow a normal distribution.However, a less widely known fact is that, as sample sizes increase, the normality assumption for the residuals is not needed. More precisely, if we consider repeated sampling from our population, for large sample sizes, the distribution (across repeated samples) of the ordinary least squares estimates of the regression coefficients follow a normal distribution. As a consequence, for moderate to large sample sizes, non-normality of residuals should not adversely affect the usual inferential procedures. This result is a consequence of an extremely important result in statistics, known as the central limit theorem.

### 5.Little or No autocorrelation in the residuals:

Autocorrelation occurs when the residual errors are dependent on each other.The presence of correlation in error terms drastically reduces model’s accuracy.This usually occurs in time series models where the next instant is dependent on previous instant.

