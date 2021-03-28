<a id = section101></a>
# Introduction

A __decision tree__ is one of most frequently and widely used supervised machine learning algorithms that can perform both __regression and classification tasks.__<br/>
The intuition behind the decision tree algorithm is simple, yet also very powerful.<br/>

Everyday we need to make numerous __decisions__, many smalls and a few big.<br>
So, Whenever you are in a dilemna, if you'll keenly observe your thinking process. You'll find that, you are unconsciously using __decision tree approcah__ or you can also say that decision tree approach is based on our thinking process. <br/>

- A decision tree __split the data into multiple sets__.Then each of these sets is further split into subsets to arrive at a __decision__.<br/>
- It is a very natural decision making process asking a series of question in a nested if then else statement.
- On each node you ask a question to further split the data held by the node. <br/>

So, lets understand what is a decision tree with a help of a real life example.<br>


Consider a scenario where a person asks you to lend them your car for a day, and you have to make a decision whether or not to lend them the car. There are several factors that help determine your decision, some of which have been listed below:

1. __Is this person a close friend or just an acquaintance?__
 - If the person is just an acquaintance, then decline the request;
 - if the person is friend, then move to next step.

2. __Is the person asking for the car for the first time?__
 - If so, lend them the car,
 - otherwise move to next step.

3. __Was the car damaged last time they returned the car?__
 - If yes, decline the request; 
 - if no, lend them the car.<br/>

[![](https://s3.amazonaws.com/stackabuse/media/decision-trees-python-scikit-learn-1.png)](https://s3.amazonaws.com/stackabuse/media/decision-trees-python-scikit-learn-1.png)

---

<a id = section201></a>
# Important Terminology related to Decision Trees

Let’s look at the basic terminology used with Decision trees:

- __Root Node__: <br/>It represents entire population or sample and this further gets divided into two or more homogeneous sets.
- __Splitting__: <br/>It is a process of dividing a node into two or more sub-nodes.
- __Decision Node__:<br/> When a sub-node splits into further sub-nodes, then it is called decision node.
- __Leaf/ Terminal Node__:<br/> Nodes do not split is called Leaf or Terminal node.

[![](https://miro.medium.com/max/688/1*bcLAJfWN2GpVQNTVOCrrvw.png)](https://miro.medium.com/max/688/1*bcLAJfWN2GpVQNTVOCrrvw.png)

- __Pruning__:<br/> When we remove sub-nodes of a decision node, this process is called pruning. You can say opposite process of splitting.
- __Branch / Sub-Tree__:<br/> A sub section of entire tree is called branch or sub-tree.
- __Parent and Child Node__:<br/> A node, which is divided into sub-nodes is called parent node of sub-nodes where as sub-nodes are the child of parent node.

---

<a id = section301></a>
# Types of Decision Trees

Types of decision tree is based on the __type of target variable__ we have. It can be of two types:

- __Categorical Variable Decision Tree__: <br/>
 - Decision Tree which has __categorical target variable__ then it called as categorical variable decision tree.
- __Continuous Variable Decision Tree__:<br/>
 - Decision Tree has __continuous target variable__ then it is called as Continuous Variable Decision Tree.<br/>
 
__Example__:<br/>
- Let’s say we have a problem to predict whether a customer will pay his renewal premium with an insurance company (__Yes/ No__).<br/> For this we are predicting values for categorical variable. So, the decision tree approach that will be used is __Categorical Variable Decision Tree.__ <br/>
- Now, suppose insurance company does not have income details for all customers. But, we know that this is an important variable, then we can build a decision tree to predict customer income based on occupation, product and various other variables.<br/> In this case, we are predicting values for continuous variable. So , This approach is called __Continuous Variable Decision Tree__.

---

<a id = section401></a>
# Concept of Homogenity

__Homogenous__ populations are __alike__ and __heterogeneous__ populations are __unlike__.<br/>
- A heterogenous population is one where individuals are __not similar__ to one another.<br/>
- For example, you could have a heterogenous population in terms of humans that have migrated from different regions of the world and currently live together. That population would likely be heterogenous in regards to height, hair texture, disease immunity, and other traits because of the varied background and genetics.

__Note__: In real world you would never get this level of homogeniety. So out of the hetrogenous options you need to select the one having maximum homoginiety. To select the feature which provide maximum homoginety we use __gini & entropy__ techniques.

What Decision tree construction algorithm will try to do is to __create a split in such a way that the homogeneity of different pieces must be as high as possible.__

__Example__

Let’s say we have a sample of __30 students__ with three variables:
1. Gender (Boy/ Girl)
2. Class (IX/ X) and,
3. Height (5 to 6 ft).<br/>

15 out of these 30 play cricket in leisure time. Now, I want to __create a model to predict who will play cricket during leisure period__? In this problem, we need to segregate students who play cricket in their leisure time based on highly significant input variable among all three.

This is where decision tree helps, it will segregate the students based on all values of three variables and identify the variable, which creates the best homogeneous sets of students (which are heterogeneous to each other). In the snapshot below, you can see that variable __Gender__ is able to identify best homogeneous sets compared to the other two variables.

![cric](https://user-images.githubusercontent.com/10387500/112757256-96415680-9006-11eb-8563-f17eb27a8071.PNG)


---

<a id = section501></a>
# How does a tree decide where to split?

The decision of making strategic splits heavily affects a tree’s accuracy. The decision criteria is different for classification and regression trees.

Decision trees use multiple algorithms to decide to split a node in two or more sub-nodes. The creation of sub-nodes increases the homogeneity of resultant sub-nodes. In other words, we can say that purity of the node increases with respect to the target variable. Decision tree splits the nodes on all available variables and then selects the split which results in most homogeneous sub-nodes.

The algorithm selection is also based on type of target variables. Let’s look at the most commonly used algorithms in decision tree:

<a id = section502></a>
 ### Gini Index
Gini index says, if we select two items from a population at random then they must be of same class and probability for this is 1 if population is pure.

- It works with categorical target variable “Success” or “Failure”.
- It performs only Binary splits
- Higher the value of Gini higher the homogeneity.
- CART (Classification and Regression Tree) uses Gini method to create binary splits.

__Steps to Calculate Gini for a split__

1. Calculate Gini for sub-nodes, using formula sum of square of probability for success and failure (1 `-` p<sup>2</sup> `-` q<sup>2</sup>).
2. Calculate Gini for split using weighted Gini score of each node of that split


__Example__: 
– Referring to example used above, where we want to segregate the students based on target variable ( playing cricket or not ). In this case we split the population using two input variables Gender and Class. Now, I want to identify which split is producing more homogeneous sub-nodes using Gini index.


__Gini for Root node__: 
 - 1 `-` (0.5 `*` 0.5) `-` (0.5 `*` 0.5) = 0.50
 
__Split on Gender__:

1. Gini for sub-node __Female__
  - 1 `-` (0.2 `*` 0.2) `-` (0.8 `*` 0.8) = 0.32
  
  
2. Gini for sub-node __Male__
  - 1 `-` (0.65 `*` 0.65) `-` (0.35 `*` 0.35) = 0.45
  
  
3. Weighted Gini for Split __Gender__ 
  -  (10/30) `*` 0.32 `+` (20/30) `*` 0.45 = 0.41
  

__Split on Class__ : 

1. Gini for sub-node __Class IX__ =
  - 1 `-` (0.43 `*` 0.43) `-` (0.57 `*` 0.57) = 0.49
  
  
2. Gini for sub-node __Class X__ =
  - 1 `-` (0.56 `*` 0.56) `-` (0.44 `*` 0.44) = 0.49
  
  
3. Calculate weighted Gini for Split __Class__  
  - (14/30) `*` 0.51 `+` (16/30) `*` 0.51 = 0.49
  
  


Above, you can see that:
__Gini score__ for Split on __Gender__ __`<`__ Gini score for Split on __Class__.<br/>
Also, __Gini score__ for __Gender__ __`<`__ Gini score for __root node__.<br/>
Hence, the __node split will take place on Gender.__

<a id = section503></a>
### Information Gain:
Look at the image below and think which node can be described easily.<br/>
I am sure, your answer is C because it requires less information as all values are similar. On the other hand, B requires more information to describe it and A requires the maximum information.<br/> In other words, we can say that __C is a Pure node, B is less Impure and A is more impure.__

![IG](https://user-images.githubusercontent.com/10387500/112757190-48c4e980-9006-11eb-8ac8-43b87c2a1d01.PNG)

Now, we can build a conclusion that:
- less impure node requires less information to describe it.
- more impure node requires more information. 

Information theory is a measure to define this degree of disorganization in a system by a parameter known as __Entropy__.
- If the sample is completely __homogeneous__, then the __entropy is zero__ and<br/>
- If the sample is an __equally divided__ (50% – 50%), it has __entropy of one__.


<a id = section504></a>
### Entropy can be calculated using formula:

![Entropy](https://user-images.githubusercontent.com/10387500/112757356-2aabb900-9007-11eb-8a1b-92d6f2dc41b9.PNG)

where,<br/>
__p__ & __q__ is __probability of success and failure__ respectively in that node.<br/> 
- __Information Gain = 1 - Entropy__.<br/>
- The model will choose the split which facilitates __maximum information gain__, which in turn means __minimum Entropy__.<br/>
- So, it chooses the split which has __lowest entropy__ compared to parent node and other splits.
- __The lesser the entropy, the better it is.__

__Steps to calculate entropy for a split__:

1. Calculate entropy of parent node
2. Calculate entropy of each individual node of split and 
3. Calculate weighted average of all sub-nodes available in split.
4. Caluclate the Information Gain in various split options w.r.t parent node
5. Choose the split with highest Information Gain.


Example: Let’s use this method to identify best split for student example.

 - __Entropy for parent node__
    - `-` (15/30) log2 (15/30) `–` (15/30) log2 (15/30) = 1.<br/>
      Here 1 shows that it is a impure node.
      
      
- __Entropy for Female node__ 
    - `-` (2/10) log2 (2/10) `–` (8/10) log2 (8/10) = 0.72 
    
    
- __Entropy for male node__
    - `-` (13/20) log2 (13/20) `–` (7/20) log2 (7/20) = 0.93
    
    
- __Entropy for split Gender__ = Weighted entropy of sub`-`nodes 
   - (10/30) `*` 0.72 + (20/30) `*` 0.93 = 0.86
   
-------------------------------------------------------------------------------------
- __Information Gain for split Gender__ = Entropy of Parent Node `-` Weighted entropy for Split Gender 
   - 1 `-` 0.86 = 0.14
-------------------------------------------------------------------------------------
   
   
   
- __Entropy for Class IX node__,
   - `-`(6/14) log2 (6/14) `–` (8/14) log2 (8/14) = 0.99
   
   
- __Entropy for Class X node__,
   - `-`(9/16) log2 (9/16) `–` (7/16) log2 (7/16) = 0.99.
   
   
- __Entropy for split Class__,
   -  (14/30) `*` 0.99 `+` (16/30) `*` 0.99 = 0.99
   

-------------------------------------------------------------------------------------
- __Information Gain for split Class__ = Entropy of Parent Node `-` Weighted entropy for Split Class 
   - 1 `-` 0.99 = 0.01
-------------------------------------------------------------------------------------

Observe that:<br/>
__Information Gain for Split on Gender > Information Gain for Split on Class__,<br/> So, __the tree will split on Gender.__<br/>

---

<a id = section601></a>
# Advantages of using Decision Tree

__Easy to Understand__: 
 - Decision tree output is very easy to understand even for people from non-analytical background. It does not require any statistical knowledge to read and interpret them. 
 - Its graphical representation is very intuitive and users can easily relate their hypothesis.
- __Less data cleaning required__: 
 - It requires less data cleaning compared to some other modeling techniques.
 - It is not influenced by outliers and missing values to a fair degree.
- __Data type is not a constraint__: 
 - It can handle both numerical and categorical variables.
- __Non Parametric Method__: 
 - Decision tree is considered to be a non-parametric method. This means that decision trees have no assumptions about the space distribution and the classifier structure.

---
<a id = section701></a>
# Shortcomings of Decision Trees
 __Over fitting__:
 - Over fitting is one of the most practical difficulty for decision tree models. This problem gets solved by setting constraints on model parameters and pruning (discussed in detailed below).
- __Not a great contributor for regression__:
 - While working with continuous numerical variables, decision tree looses information when it categorizes variables in different categories.
 
 ---









