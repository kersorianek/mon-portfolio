---
layout: post
title: Building a web app to predict Kickstarter campaign success
image: https://raw.githubusercontent.com/Ekram49/Kickstarter-blogpost/master/Images/kickstarter-logo.jpg
---
As a Lamdaschool data science student, me along with other data science students was tasked to create a web app that would predict the success/failure of a Kickstarter campaign. It was a fun project to do and it felt great to create a fully functioning useful web app within just four days!
Investing in a Kickstarter campaign is not risk free. If a campaign fails, the investors loose all the money. So, you have to look at a campaign to determine the possibility of the campaign being successful before putting your money on a campaign. Only if there was someone who has a great intuition of determining which one’s will succeed! Lucky for you our app can do exactly that. 

![Crepe](https://raw.githubusercontent.com/Ekram49/Kickstarter-blogpost/master/Images/thinking.jpg)

We have taken the data of all the Kickstarter campaigns from a website named [Web Robots](https://webrobots.io/kickstarter-datasets/) Which contains all the information we needed to create a predictive model, that would facilitate our app with the power to predict the success/failure of a Kickstarter campaign based on some features of the given campaign.

The features we used to create our model was:

•	Category

•	Description length

•	Campaign goal (in USD)

•	Campaign length (days)

•	Staff pick

![Crepe](https://raw.githubusercontent.com/Ekram49/Kickstarter-blogpost/master/Images/feature%20importances.PNG)

Exploring the datasets, we found out that out of 209,445 Kickstarter campaigns:


•	121,651 were successful

•	73,683 failed

•	8,904 were cancelled

•	5,207 are live

![creep](https://raw.githubusercontent.com/Ekram49/Kickstarter-blogpost/master/Images/state.PNG)

After some more Exploratory data analysis, we Used “Random Forest Classifier” to create our predictive model which gave us around 75.3% test accuracy which we were pretty satisfied with considering how many different variables can affect the success of a campaign which makes creating a super accurate model impossible.

![Crepe](https://raw.githubusercontent.com/Ekram49/Kickstarter-blogpost/master/Images/app-1.PNG)

![Crepe](https://raw.githubusercontent.com/Ekram49/Kickstarter-blogpost/master/Images/app-2.PNG)

To use our predictive model, we developed a [Flask app](https://ds-15-ks-2.herokuapp.com/) which allows you to put the features as input and spit out the probability of your campaign being successful.

After spending a good amount of time analyzing the data, creating model and app, we would suggest if you want to start a Kickstarter campaign, or you want to invest in one, make sure:

•	Have a reasonable goal

•	Don’t have too long campaign

•	Have a good description about the campaign

![Crepe](https://raw.githubusercontent.com/Ekram49/Kickstarter-blogpost/master/Images/best-of-luck-picture-with-thumb.jpg)

## Credits:

•	Antonio Peterson - Project lead

•	Jace Hambrick - Data Engineer

•	Jashim Rashid - Data Engineer

•	Luis Urene - Machine Learning Engineer

•	Ekram Ahmed(Myself) - Machine Learning Engineer

## Resources:

•	[Github repo of the project](https://github.com/Build-Week-Kickstarter-Success-2/DS)

•	[Datasets](https://webrobots.io/kickstarter-datasets/)

•	[App](https://ds-15-ks-2.herokuapp.com/)
