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

# Important Terminology related to Decision Trees

Let’s look at the basic terminology used with Decision trees:

- __Root Node__: <br/>It represents entire population or sample and this further gets divided into two or more homogeneous sets.
- __Splitting__: <br/>It is a process of dividing a node into two or more sub-nodes.
- __Decision Node__:<br/> When a sub-node splits into further sub-nodes, then it is called decision node.
- __Leaf/ Terminal Node__:<br/> Nodes do not split is called Leaf or Terminal node.
