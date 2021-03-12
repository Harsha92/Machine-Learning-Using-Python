
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



In other words:

- Logistic regression outputs the __probabilities of a specific class__.
- Those probabilities can be converted into __class predictions__.


The logistic function has some nice properties:

- Takes on an __"s"__ shape
- Output is bounded by __0 and 1__<br/>

# Applications of Logistic Regression

Logistic Regression was used in __biological sciences__ in early twentieth century. It was then used in many social science applications. For instance,
- The Trauma and Injury Severity Score (TRISS), which is widely used to __predict mortality in injured patients__, was originally developed by Boyd et al. using logistic regression.<br/> 
- Many other medical scales used to __assess severity__ of a patient have been developed using logistic regression.<br/>
- Logistic regression may be used to __predict the risk of developing a given disease__ (e.g. diabetes; coronary heart disease), based on observed characteristics of the patient (age, sex, body mass index, results of various blood tests, etc.).<br/>

Now a days, Logistic Regression have the following applications 
1. Image segementation and  categorization
2. Geographic image processing
3. Handwriting recognition
4. Detection of  myocardinal infarction
5. Predict whether a person is depressed or not based on a bag of words from corpus. 

The reason why logistic regression is widely used despite of the state of the art of deep neural network is that logistic regression is very __efficient__ and does __not__ require too much __computational resources__, which makes it __affordable__ to run on production.
