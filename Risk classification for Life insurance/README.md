
<a name = Section101></a>
# Project Description

In this dataset, we are provided over a hundred variables describing attributes of life insurance applicants. The task is to predict the "Response" variable for each Id in the test set. "Response" is an ordinal measure of risk that has 8 levels.

We will do a binary classification by altering the target variable. Based on the attributes of customers, will the life insurance policy be approved or not i.e.yes(1) or no(0).we will turn this Multiclass classification into Binary classification.
We are making 0 to 7 as one class (0 - which mean approved with additional terms and conditions or rejected) and 8 as another class (1 - which means approved)

---

<a name = Section301></a>
# Data Description


| Feature  | Description  |
| ------------ | ------------ |
| Id  | A unique identifier associated with an application.  |
| Product_Info_1-7  | A set of normalized variables relating to the product applied for  |
| Ins_Age  | Normalized age of applicant  |
| Ht  | Normalized height of applicant  |
| Wt   | Normalized weight of applicant  |
| BMI   | Normalized BMI of applicant  |
| Employment_Info_1-6  |  A set of normalized variables relating to the employment history of the applicant. |
| InsuredInfo_1-6  |  A set of normalized variables providing information about the applicant.  |
| Insurance_History_1-9  |  A set of normalized variables relating to the insurance history of the applicant. |
| Family_Hist_1-5  |  A set of normalized variables relating to the family history of the applicant. |
| Medical_History_1-41  | A set of normalized variables relating to the medical history of the applicant.  |
| Medical_Keyword_1-48  |  A set of dummy variables relating to the presence of/absence of a medical keyword being associated with the application. |
|Response | This is the target variable, an ordinal variable relating to the final decision associated with an application  |

---

<a name = Section501></a>
# Feature Engineering


---

<a name = Section701></a>
# Model Comparission

- From the below results we can see that the Random Forest with Hyperparameter tuning has given us the best performance

[![Model Comparission](https://raw.githubusercontent.com/Harsha92/Machine-Learning-Using-Python/main/Risk%20classification%20for%20Life%20insurance/Images/Model%20Comparision.PNG "Model Comparission")](https://raw.githubusercontent.com/Harsha92/Machine-Learning-Using-Python/main/Risk%20classification%20for%20Life%20insurance/Images/Model%20Comparision.PNG "Model Comparission")

---
