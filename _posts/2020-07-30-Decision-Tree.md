---
layout: post
title: Building a Decision Tree Algorithm
image: https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/tree.jpg
---
## Decision tree:
A decision tree is a decision support tool that uses a tree-like graph or model of decisions and their possible consequences, including chance event outcomes, resource costs, and utility. It is one way to display an algorithm that only contains conditional control statements.

## Some info:

**A tree has a root node**
**A node can have left branch and right branch.**
**Lowest layer nodes do not have any branches (leaf nodes)**

## Steps of implementing Decision Tree:

# Implement branches:

We begin by adding a constructor to the class and initialize the left and right branches to None.

## Finding the optimal split:

To find the optimal split, we need to have a unit of measure to quantify the impurity and in the information gain at each level. There are many measures of impurity, we will use Gini impurity.

![Crepe](https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/01.PNG)

In the first equation k is number of classes in the target attribute and p is the probability of the class at the node.

In the second equation k is number of classes in the target attribute, r is the number of rows in the node and n is the number of rows in the dataset.

We are going to implement Impurity and Information Gain

![Crepe](https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/02.PNG)

In order to find the best split, we need to get the best split in each feature and use the one with the most information gain. First let us see the implementation for a single feature

![Crepe](https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/03.PNG)

We must then repeat this for all the features, to find the best split across all of them.

![Crepe](https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/04.PNG)

## Create Branches:

Now that we have identified the split, let us create the branches.

![Crepe](https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/05.PNG)

## Fit the data:

Now that we created our decision tree, we need to write a function that will fit the data

![Crepe](https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/06.PNG)

# Predict:

In order to predict the probabilities of the test data, let us create two function, one to iterate through each row while the other to traverse the tree for a row and find the prediction. The latter method invokes iteratively till it reaches a leaf node.

![Crepe](https://raw.githubusercontent.com/Ekram49/bw_decision_tree/master/Images/07.PNG)

You can find my whole code [here](https://github.com/Ekram49/bw_decision_tree)

## Conclusion

The aim of this project is not to build a highly efficient algorithm ( [sklearn](https://scikit-learn.org/stable/modules/tree.html) got that covered.) The goal was to get a better understanding of how decision tree works by creating one from scratch. Most of the time we use various pre-built algorithm for convenience, but creating one can really give you an understanding about what's really happening under the hood. 
