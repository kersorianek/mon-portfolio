---
layout: post
title: The beauty of Boosting
subtitle: how "boosting" has aided the world of machine learning
cover-img: /assets/img/gbm_pic.png
thumbnail-img: /assets/img/gbm_pic.png
share-img: /assets/img/path.jpg
tags: [books, test]
---

Consider that you are an amateur bettor and started betting for money recently. Having lost a number of your initial bets, you decide to ask an expert bettor to reveal his betting strategy. The expert comes up with a number of rules-of-thumb he considers to have helped him make educated bets in the past. Unsurprisingly, he gives you a collection of very modest rules which he claims to have considered in bets: such as bet on the horse that has the highest win-loss ratio and bet on the horse that everyone else has bet on.  Although these rules seem rudimentary, it looks reasonable to expect the rules to provide an educated decision at least marginally better than random guessing. Having had some computer science and statistics training, you want to come up with a program to make better bets with all the rules that you have collected. You are primarily faced with two problems,

	1. How should I assemble the races to extract the rules of thumb that will be most useful for my betting?
	2. How can I combine all the rules of thumb into a one unified rule to be used in future betting?
 
Boosting refers to the process of synthasizing an accurate prediction rule by combining rules-of-thumb that are at least marginally better than random guessing through a process similar to the one explained above. 
Boosting belongs to the family of ensemble learning algorithms which give credence to the idea of “wisdom of crowds”. In a machine learning context this means that a collective decision of a number of models is always better than the prediction of a single model. The invent of a number of ensemble learning algorithms in 1990s such as AdaBoost helped lift the field of machine learning to the next level. Researchers such as Leo Breiman, Yoav Freund, Robert Schapire made early discoveries in ensemble learning by introducing the first stable versions of bagging and boosting. Buoyed by the dramatic increase of data and computation, more recent researchers have come up with a number of algorithms that built on the original premise of boosting. The data scientists today enjoy the benefits of using powerful algorithms such as XGBoost, Gradient Boosting Machine and LightGBM which are highly accurate, distributed and scalable.

### An example case of AdaBoost
The mechanics of boosting can best be described through the AdaBoost algorithm which was introduced in 1995 by Freund and Schapire. As the name suggests, Ada-Boost aims to ‘adapt’ to the error rates of the training examples. Therefore “Ada” is the shortened acronym for “Adaptive”. A simplified version of the psudocode of the algorithm is given below. Lets look at a case of a binary classification which has a decision tree base learner.

Training examples:  x_m,y_m Where they are normally distributed
Initialize the set of weights which is a distribution: D_1 (i)=1/m 
For t = 1,….., T:
	Train a weak learner using the initial weights D_t
	Calculate the error of the weak learner (hypothesis) ∈_t
	Choose a learning rate based on the error : Learning rate low if error is low, learning rate high if error is high : α_t 
	Update next time period’s weights D_(t+1) :
	D_t  × e^(-αt)  if correctly classified,
	D_t  × e^αt    if incorrectly classified,
	Multiply by a normalizing factor Z_t

Note that weights are updated every time a classifier is run using the learning rate. Usually the learning rate or the importance α_t>0   if ∈_t<1/2 . This ensures the model focusses its effort on examples that are difficult to classify. This adjustment factor also creates an effect where every individual learner is dependent on all the all the other learners that preceded it. This is one of the more prominent differences between bagging and boosting where each bagging learner is independent of others.

### Differences between bagging and boosting

Bagging and boosting are both ensemble algorithms and were invented in early 1990s. The two approaches manipulate the training datasets in order to construct different base learners. They aim at improving the prediction power of models by combining base learners through voting. Both algorithms can be used for classification and regression problems.

Whilst there are a number of similarities between boosting and bagging, the mechanics of them are essentially different. Bagging or bootstrapped aggregation is based on sampling-with-replacement. Bagging creates a number of training datasets using sampling with-replacement whereas boosting uses the entire training set without any sampling in all the rounds. It also maintains a distribution of weights over the training examples whereas the importance (or weights) assigned to each training example is the same in bagging. The different weights result in different base classifiers whereas in bagging each classifier is similar. The sequential process of boosting creates a set of interlinked learners whereas bagging result in independent base learners. 

### Empirical results for boosting algorithms

Boosting is an algorithm that has been empirically tested a number of times. The problems that were addressed using boosting are not only limited to regression, but also includes binary and multiclass classification, text categorization, ranking problems and NLP ranking problems. An interesting property of boosting is its performance on outliers. The weights of a boosting algorithm tends to be concentrated on difficult examples. These “difficult” examples are often the instances that appear to be behaving differently from the rest of the population. Based on this insight, one can use the weights of a boosting algorithm to identify outliers or the examples that are misclassified in a training space. This also signifies that like most other algorithms, the performance of a boosting algorithm will suffer in the presence of too many outliers. However, more recent algorithms such as “Gentle Adaboost” and “BrownBoost” puts less emphasis on outliers, guiding its effort on more “plausible” examples.

### Weaknesses of boosting

Boosting is not without its weaknesses. The performance of boosting is highly dependent on the quantity of data. A more simpler model such as OLS regression or a decision tree could be a better fit for little data. The accuracy is also as good as the set of hypothesis that you provide. The weak hypothesis which are too weak will not lead to a great composite classifier. Compared to a more simplistic algorithm such as linear regression, it is more computationally expensive and take longer to train. The empirical literature for boosting have been presented in the perspective of performance and computational cost but not the interpretability. Therefore boosting is less equipped to tackle descriptive analytics.

Boosting is a method, given sufficient data, can produce a strong learner using a set of moderately accurate hypothesis. It essentially aims at finding a weak set of hypothesis that requires to be only slightly better than random guessing compared to finding a single hypothesis that needs to be accurate over the entire training set. This theoretical guarantee sparked a major shift in machine learning mindset which paved way to the invent of a number of related algorithms in later generations. The use of numerous boosting algorithms in some of the today’s hardest machine learning problems stand proof to how it has contributed the field of machine learning.
