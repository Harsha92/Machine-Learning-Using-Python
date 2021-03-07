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
