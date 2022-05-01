---
layout: post
title: Linear regression - Why it is modeling E[Y]?
tags: [Linear Model]
comments: true
---
One questions has bothered me for quite a while: 

Why textbooks claim, for Linear Regression, we are essectially modeling the expected value of the response Y, i.e, $E[Y]$?


if we vaguely recall the regression equation for simple linear regression (SLM), 

$f(x) = b_0 + b_1x$

what it has to do with expected value $E[Y]$?

After reviewing on the topics a bit, I quickly realise I am mixing up things and i want to wirte a short post on it. In case anyone out there also get a bit rusted on the topic or a bit new into statsical modeling, hopefully it could help get their head around this topic.

In statsical studies, we believe there is certian relation between input variables/predictors, X and the response Y. In a general form

$Y = f(X) + \epsilon$

f is some function of X.

At linear models, one assumption is there is a approximatedly a linear relationship between X and Y. 

$f(X) = \beta_0 + \beta_1 X$

$Y = \beta_0 + \beta_1 X + \epsilon$

If we take expect value on those side of the equation:

$E[Y] = E[ \beta_0 + \beta_1 X + \epsilon]$

$= \beta_0 + \beta_1 X + E[\epsilon]$ 

$= \beta_0 + \beta_1 X$

$=f(X)$

*<span style="color:grey;"> $E[\epsilon]=0$ is one of the assumption of linear regression.</span>*

f(X) also called **popultion regression line**. However, since we only have access to sampled data, we are actually estimating this underlying popultion line with the regression equation
$\tilde f(x) = b_0 + b_1x$

therefore, going back to the original question, modeling/estimating E[Y] is modeling f(X).

This graph also serves a great interpretation
<img src="https://online.stat.psu.edu/stat462/sites/onlinecourses.science.psu.edu.stat462/files/02simple/gpatestscore/index.jpg" title="population line" />&nbsp;   
Each $Y_i$ is draw from the normal distribution $N(\beta_0 + \beta_1X_i,\sigma^2)$ , when i is fixed, every draw of $Y_i$ will be different due to the randomness, but they center around the fixed value $\beta_0 +\beta_1X_i$.





