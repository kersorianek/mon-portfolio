---
layout: page
title: My Projects
subtitle: An Economist's Journey to a Senior Data Scientist
---

Studying economics lead me to the paradox of choice: you feel qualified to pick up an innumerable number of career paths, yet you are not a perfect fit to one. Data science and analytics is something I felt I had an inner calling. 

## 1. Image Classification of Bottle Coolers

This project involved bringing massive value to the business through identifying faulty and non-performing bottle coolers automatically through classifying bottle cooler pictures. I was amazed by how difficult it is to find faulty coolers that were deployed in the market. It was time consuming to manually go through all the bottle cooler images and pick ones that need replenishing and repairing. This machine learning project harnessed the power of convolution neural network and Inception V3 deep neural network architecture. The insights about cooler productivity was generated through classifying the cooler pictures into 4 categories: good, bad, worse and non-fuctional. Involved in model training, model tuning and data pipeline building. 

##### Technologies used:
- Python
- R
- Tensorflow
- deep learning: convolution neural networks
- GIT

##### Read more on Medium:
https://medium.com/@ekanaypo/how-deep-learning-and-tensorflow-helps-a-soft-drinks-business-grow-486212b3bcb2 
([https://link-url-here.org](https://medium.com/@ekanaypo/how-deep-learning-and-tensorflow-helps-a-soft-drinks-business-grow-486212b3bcb2))

  
## 2. Supply-side planning: DNA data for precise sales prediction

A large meat producer faced a grave problem: how to plan the supply of different grades of meats when the quality of the cut is not known before they are processed? This affected all the other sections in the organization as an accurate estimation of revanue was not possible. The data science team identified that an accurate prediction of the grade of the animal would solve the problem. Used an Xgboost machine learning model to accurately predict the meat grade using animal DNA readings. I was involved in the data manipulation process, model building and front end shiny dashboard.

##### Technologies used:
- R
- Shiny interactive dashboard
- SQL
- XgBoost
  

## 3. Retail promotional optimization

Used machine learning to predict the best promotions to be run in supermarket chains in order to maximize margins. The usecase generated 40% increase in ROI of promotions. The client is a large beverages manufacturer. The project involved the following steps:
1. Creating a baseline level of performance using past non-promotional periods: use of exponential smoothing.
2. identified the uplift volume of past promotions by considering effects such as cannibalization, forward buying, anticipated buying, and the developed baseline.
3. Once the ROI of past promotions is identified, used a random forest model to learn the intricate patterns of successful promotions.
4. Once the patterns are identified, the model is able to predict the promotions that will potentially be successful in the future.

##### Technologies used:
- PySpark
- Mlflow
- Spark machine learning
- PowerBi
- SQL
- Machine learning models: Decision tree, Random forest, Gradient Boosting Algorithm
