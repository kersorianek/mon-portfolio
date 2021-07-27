---
layout: post
title: Thoughts on logistic regression - Theory
tags: [Linear Model]
comments: true
---

I was reading the chapter on logistic regression from DS for business and the author throws out a equation 
                                        equation (1)
​

I wonder where did the eqivalence relation comes from so I googled a bit and found this link on stackoverflow
[https://stats.stackexchange.com/questions/503319/why-are-log-odds-modelled-as-a-linear-functio](https://stats.stackexchange.com/questions/503319/why-are-log-odds-modelled-as-a-linear-function)n 
This is asking exactly the same question.  Still I feel a bit confused about the voted corrected answer.
​

The following are some of the thoughts I have:


 is also called logit function. I rewrite it as , which is a function takes a probablity value p and generate some values in real number. Probablity can only takes value within 0 and 1 and result of log takes from miuns infinity to infinity.
If you thinks back on the purpose of logitsic regresssion, you will realize what we want is exactly the opposite: we want is a function that takes any real number and generate a result between 0 and 1.
One way to do so, is to take the inverse of , which will switch its x-axis and y-axis.
​

                                                 equation(2)
now we have an equation of y, which takes values in real numbers and maps them in to [0,1]. We denote the funtcion as: 

you might wonder what is the input varible y? It is the linear combination of independent variable X. 

