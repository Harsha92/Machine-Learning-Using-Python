
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



