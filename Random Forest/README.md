
# Random Forest


__Random Forest__ is considered to be the __panacea__ of all data science problems. On a funny note, when you can’t think of any algorithm (irrespective of situation), use random forest!

In Random Forest, we grow __multiple trees__ as opposed to a single tree in CART model . To classify a new object based on attributes, each tree gives a classification and we say the tree “votes” for that class. __The forest chooses the classification having the most votes__ (over all the trees in the forest) and in case of __regression__, it takes the __average of outputs by different trees.__

Random Forest is a versatile machine learning method capable of performing __both regression and classification tasks__. It also undertakes dimensional reduction methods, treats missing values, outlier values and other essential steps of data exploration, and does a fairly good job. It is a type of __ensemble learning__ method, where __a group of weak models combine to form a powerful model.__

---

# Real Life Analogy

Imagine a guy named Andrew, that want’s to decide, to which places he should travel during a one-year vacation trip. He asks people who know him for advice. First, he goes to a friend, tha asks Andrew where he traveled to in the past and if he liked it or not. Based on the answers, he will give Andrew some advice.


This is a typical __decision tree algorithm approach__. Andrews friend created rules to guide his decision about what he should recommend, by using the answers of Andrew.


Afterwards, Andrew starts asking more and more of his friends to advise him and they again ask him different questions, where they can derive some recommendations from. Then he chooses the places that where recommend the most to him, which is the typical 
__Random Forest algorithm approach__.

---
# Wisdom of Crowd


“The Wisdom of Crowds” is an idea, summarized in the 2004 book by __James Surowiecki__ by the same name, which states that __the aggregate information in a group often leads to a better decision than any single member of the group.__

- It’s something that’s been empirically _observed_ in many different areas of _social science_, and if some basic initial conditions are met, it usually holds up pretty well in the real world.
- The premise is this – if you take a large enough group of people, all with independent judgments, and all with access to different levels and amounts of information, the overall group’s average judgment is usually better than any single individual judgment. 
- There have been many famous cases of Wisdom of Crowds at play – from guessing the weight of an ox at a county fair to asking the audience in the popular game show, __Who Wants To Be A Millionaire__.


If you are running a Random Forest model in your job or class, and you sift through some of the statistics and mathematics behind it, you are in effect applying some of the core concepts of the Wisdom of Crowds in your work. In his book, James Surowiecki lays out some of the basic elements that are required for the Wisdom of Crowds to work. Here’s how it compares to what Random Forest is actually doing.

![WC](https://user-images.githubusercontent.com/10387500/112758209-abb87f80-900a-11eb-84bb-0e21d6defab1.PNG)


- Statistically speaking, Random Forest is simply trying to __reduce the variance in prediction by averaging a large number of independent, uncorrelated, individual predictions__
- Philosophically, Random Forest is simply applying many of the ideas behind the __Wisdom of Crowds__.

---
# Concept behind random forest

The random forest is a model made up of many decision trees. Rather than just being a forest though, this model is random because of two concepts:

1. Random sampling of data points
2. Splitting nodes based on subsets of features

### Random Sampling


- One of the keys behind the random forest is that __each tree trains on random samples__ of the data points. 
- The samples are drawn with _replacement_ (known as __bootstrapping__) which means that some samples will be trained on in a single tree multiple times (we can also disable this behavior if we want).
- The idea is that by training each tree on different samples, although __each tree__ might have __high variance__ with respect to a particular set of the training data, overall, the __entire forest __will have __low variance__.
- This procedure of training each individual learner on different subsets of the data and then averaging the predictions is known as __bagging__, short for bootstrap aggregating.

![RS](https://user-images.githubusercontent.com/10387500/112758263-0225be00-900b-11eb-966c-1df3ffc6717f.PNG)


To more clearly understand bagging summarised below are the steps to follow: 

1. __Create Multiple DataSets__:
    - Sampling is done with replacement on the original data and new datasets are formed.
    - The new data sets can have a fraction of the columns as well as rows, which are generally hyper-parameters in a bagging model
    - Taking row and column fractions less than 1 helps in making robust models, less prone to overfitting
2. __Build Multiple Classifiers__:
    - Classifiers are built on each data set.
    - Generally the same classifier is modeled on each data set and predictions are made.
3. __Combine Classifiers__:
    - The predictions of all the classifiers are combined using either mean or mode value depending on the problem at hand.
    - Generally __mean__ are used for __regression__ problems and __mode__ is used for __classification__ problems.  
    - The combined values are generally more robust than a single model.
    
<a id = randomsubset></a>

### 4.4.2 __Random Subsets of Features__

- Another concept behind the random forest is that only a __subset__ of all the __features__ are considered for splitting each node in each decision tree. Generally this is set to __sqrt(n_features)__ meaning that at each node, the decision tree considers splitting on a sample of the features totaling the square root of the total number of features. 
- The random forest _can_ also be trained considering __all the features__ at every node. (These options can be controlled in the Scikit-Learn random forest implementation).


The random forest combines hundreds or __thousands of decision trees__, trains each one on a __slightly different set of the observations__ (sampling the data points with replacement) and also __splits nodes in each tree considering only a limited number of the features.__ The final predictions made by the random forest are made by __averaging the predictions of each individual tree.__


---
# Advantages and Shortcomings:

__Advantages__


- It can be used for __both regression and classification__ tasks and that it’s easy to view the relative importance it assigns to the input features.

- Random forest classifier __handle the missing values__ on its own.

- Random Forest is also considered as a very handy and easy to use algorithm, because it’s __default hyperparameters often produce a good prediction result__. The number of hyperparameters is also not that high and they are straightforward to understand.

- One of the big problems in machine learning is overfitting, but most of the time this won’t happen that easy to a random forest classifier. That’s because if there are __enough trees__ in the forest, the classifier __won’t overfit__ the model.

__Shortcomings__

- The main limitation of Random Forest is that a __large number of trees__ can make the algorithm __slow and ineffective for real-time predictions.__ In general, these algorithms are fast to train, but quite slow to create predictions once they are trained. A more accurate prediction requires more trees, which results in a slower model. In most real-world applications the random forest algorithm is fast enough, but there can certainly be situations where run-time performance is important and other approaches would be preferred.

- Random Forest is a predictive modeling tool and __not a descriptive tool__. That means, if you are looking for a description of the relationships in your data, other approaches would be preferred.

- Random Forest can feel like a __black box approach for statistical modelers__ – you have __very little control__ on what the model does. You can at best – try different parameters and random seeds!





