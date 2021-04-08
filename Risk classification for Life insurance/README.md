
<a name = Section101></a>
# Problem Statement

In this dataset, we are provided over a hundred variables describing attributes of life insurance applicants. The task is to predict the "Response" variable for each Id in the test set. "Response" is an ordinal measure of risk that has 8 levels.

We will do a binary classification by altering the target variable. Based on the attributes of customers, will the life insurance policy be approved or not i.e.yes(1) or no(0).we will turn this Multiclass classification into Binary classification.
We are making 0 to 7 as one class (0 - which mean approved with additional terms and conditions or rejected) and 8 as another class (1 - which means approved)

---

<a name = Section701></a>
# Model Comparission

- From the below results we can see that the Random Forest with Hyperparameter tuning has given us the best performance

[![Model Comparission](https://raw.githubusercontent.com/Harsha92/Machine-Learning-Using-Python/main/Risk%20classification%20for%20Life%20insurance/Images/Model%20Comparision.PNG "Model Comparission")](https://raw.githubusercontent.com/Harsha92/Machine-Learning-Using-Python/main/Risk%20classification%20for%20Life%20insurance/Images/Model%20Comparision.PNG "Model Comparission")

---
