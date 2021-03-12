
# Introduction to Logistic Regression

Logistic regression is a techinque used for solving the __classification problem__.<br/> And Classification is nothing but a problem of __identifing__ to which of a set of __categories__ a new observation belongs, on the basis of _training dataset_ containing observations (or instances) whose categorical membership is known. <br/>For example to predict:<br/> __Whether an email is spam (1) or not (0)__ or,<br/> __Whether the tumor is malignant (1) or not (0)<br/>__


Both Linear regression and Logistic regression are __supervised learning techinques__. But for the _Regression_ problem the output is __continuous__ unlike the _classification_ problem where the output is __discrete__. <br/>
- Logistic Regression is used when the __dependent variable(target) is categorical__.<br/>
- __Sigmoid function__ or logistic function is used as _hypothesis function_ for logistic regression. Below is a figure showing the difference between linear regression and logistic regression, Also notice that logistic regression produces a logistic curve, which is limited to values between 0 and 1. <br/> 
[![](https://miro.medium.com/max/3750/1*G3imr4PVeU1SPSsZLW9ghA.png)](https://miro.medium.com/max/3750/1*G3imr4PVeU1SPSsZLW9ghA.png)

---
# Mathematics behind Logistic Regression

The __odds__ for an event is the __(probability of an event occuring) / (probability of event not occuring)__:

For __Linear regression__: continuous response is modeled as a linear combination of the features: __y = β0 + β1x__<br/>
For __Logistic regression__: log-odds of a categorical response being "__true__" (1) is modeled as a linear combination of the features:

The Probability P can be found as below

[![](https://camo.githubusercontent.com/c5e464fcd1955db626a19adf846bfb57ab5007e607b040e8f07ac9f579c8a5a1/687474703a2f2f666163756c74792e6361732e7573662e6564752f6d6272616e6e69636b2f72656772657373696f6e2f676966732f6c6f382e676966)](https://camo.githubusercontent.com/c5e464fcd1955db626a19adf846bfb57ab5007e607b040e8f07ac9f579c8a5a1/687474703a2f2f666163756c74792e6361732e7573662e6564752f6d6272616e6e69636b2f72656772657373696f6e2f676966732f6c6f382e676966)

Shown below is the plot showing __linear model__ and __logistic model__: 

[![](https://saedsayad.com/images/LogReg_1.png)](https://saedsayad.com/images/LogReg_1.png)
