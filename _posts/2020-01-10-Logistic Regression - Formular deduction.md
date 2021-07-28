---
layout: post
title: Thoughts on logistic regression - Theory
tags: [Linear Model]
comments: true
---

I was reading the chapter on logistic regression from DS for business and the author throws out a equation

<a href="https://www.codecogs.com/eqnedit.php?latex=log\frac{p}{1-p}&space;=&space;w_0&space;&plus;&space;WX" target="_blank"><img src="https://latex.codecogs.com/gif.latex?log\frac{p}{1-p}&space;=&space;w_0&space;&plus;&space;WX" title="log\frac{p}{1-p} = w_0 + WX" /></a>&nbsp;                                                           equation (1)
​

I wonder where did the eqivalence relation comes from so I googled a bit and found this link on stackoverflow
[https://stats.stackexchange.com/questions/503319/why-are-log-odds-modelled-as-a-linear-functio](https://stats.stackexchange.com/questions/503319/why-are-log-odds-modelled-as-a-linear-function)n 
This is asking exactly the same question.  Still I feel a bit confused about the voted corrected answer.
​

The following are some of the thoughts I have:

<a href="https://www.codecogs.com/eqnedit.php?latex=log\frac{p}{1-p}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?log\frac{p}{1-p}" title="log\frac{p}{1-p}" /></a> is also called logit function. I rewrite it as <a href="https://www.codecogs.com/eqnedit.php?latex=Logit&space;(p)" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Logit&space;(p)" title="Logit (p)" /></a>, which is a function takes a probablity value p and generate some values in real number. Probablity can only takes value within 0 and 1 and result of log takes from miuns infinity to infinity.
If you thinks back on the purpose of logitsic regresssion, you will realize what we want is exactly the opposite: we want is a function that takes any real number and generate a result between 0 and 1.
One way to do so, is to take the inverse of <a href="https://www.codecogs.com/eqnedit.php?latex=log\frac{p}{1-p}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?log\frac{p}{1-p}" title="log\frac{p}{1-p}" /></a>, which will switch its x-axis and y-axis.


<a href="https://www.codecogs.com/eqnedit.php?latex=P(y)=\frac{e^y}{1&plus;e^y}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?P(y)=\frac{e^y}{1&plus;e^y}" title="P(y)=\frac{e^y}{1+e^y}" /></a>&nbsp;                                                                      equation(2)


now we have an equation of y, which takes values in real numbers and maps them in to [0,1]. We denote the funtcion as: 
<a href="https://www.codecogs.com/eqnedit.php?latex=P(y)=\frac{e^y}{1&plus;e^y}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?P(y)=\frac{e^y}{1&plus;e^y}" title="P(y)=\frac{e^y}{1+e^y}" /></a> 

you might wonder what is the input varible y? It is the linear combination of independent variable X. 

<a href="https://www.codecogs.com/eqnedit.php?latex=Y(x)&space;=&space;w_0&space;&plus;&space;wx" target="_blank"><img src="https://latex.codecogs.com/gif.latex?Y(x)&space;=&space;w_0&space;&plus;&space;wx" title="Y(x) = w_0 + wx" /></a>

<a href="https://www.codecogs.com/eqnedit.php?latex=P(Y(x))&space;=&space;P(w_0&space;&plus;&space;wx)&space;=&space;\frac{e^{w_0&plus;wx}}{1&plus;e^{w_0&plus;wx}}" target="_blank"><img src="https://latex.codecogs.com/gif.latex?P(Y(x))&space;=&space;P(w_0&space;&plus;&space;wx)&space;=&space;\frac{e^{w_0&plus;wx}}{1&plus;e^{w_0&plus;wx}}" title="P(Y(x)) = P(w_0 + wx) = \frac{e^{w_0+wx}}{1+e^{w_0+wx}}" /></a>

