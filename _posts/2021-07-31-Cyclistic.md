---
layout: post
title: How Does a Bike-Share Navigate Speedy Success?
subtitle: A case study on 'Cyclistic' bike-share company
image: https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/Cyclistic.png
---

## Introduction 

Welcome to the Cyclistic bike-share analysis case study! This is a capstone project I completed as part of my Google Data Analytics Professional Certificate.
In this study I acted as a junior data analyst working in the marketing analyst team at Cyclistic, a bike sharing company at Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. 
Therefore, our team wanted to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, our team would design a new marketing strategy to convert casual riders into annual members. 
In order to do that, however, the marketing analyst team needed to better understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could affect their marketing tactics. So, it was my duty as a data analyst to find answers to those questions from the data and give recommendations based on the analysis.


## Objective of the analysis

The main objectives of the analysis were to answer these three questions:

•	How do annual members and casual riders use Cyclistic bikes differently?

•	Why would casual riders buy Cyclistic annual memberships?

•	Weather data

•	How can Cyclistic use digital media to influence casual riders to become members?


## About the data

The data I received was the trip data of all users in the year 2018. The data came in four different datasets, which contained quarterly data of the year. Some of the important features of the data include Trip start and end time, station names where trips started/ended and the user-type (Subscriber/Customer).


## Data cleaning and feature engineering

Our website has some useful functionality that can help the user to gather necessary info about a city. Upon searching for a city:

•	Giving same column names to all four datasets so that they can be joined together.

•	Removing rows where trip-duration is negative.

•	Removing outliers by getting rid of rows that contained the top 1% and bottom 1% values of trip duration.



![Crepe](https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/outliers.PNG)



Some of the new features I created include:

•	 Ride length(minute) from ‘start_time’ and ‘end_time’ column.

•	 Day of the week (Mon-Fri) from ‘start_time’ column.

•	 Month from ‘start_time’ column.

•  Season from ‘start_time’ column.



![Crepe](https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/seasons.PNG)



## Data Analysis

One of the most important tasks of mine was to understand our users. To do that I wanted to figure out their riding patterns. I found that even though the vast majority of our users are already subscribers, but the casual riders have a significant overall ride-time.



![Crepe](https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/ratio.png)



So, I dug deeper and found that most of the subscribers tend to have shorter rides where the ride time of casual riders much longer and diverse.



![Crepe](https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/trip_duration.png)



Next, I wanted to find out how trip-duration differs based on the day of the week.



![Crepe](https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/daily.png)



I found out that as expected the casual riders tend to ride more on the weekends. But interestingly enough, the subscribers also tend to ride more over the weekends that weekdays.

I also wanted to see how the time of the year affects trip duration.



![Crepe](https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/monthly.png)



It seems like trip duration tend to go high in the Spring time and tends to stay high in the summer, and starts to fall before winter. But it varies more for the casual users, and the duration is relatively constant for the Subscribers.

Finally, I generated a table containing the top 10 stations used by the customers and subscribers.



![Crepe](https://raw.githubusercontent.com/Ekram49/Ekram49.github.io/master/img/Cyclistic/top_places.PNG)



## Summary

In a few words, the summary of my analysis:

•	 Casual riders tend to ride longer than subscribers.

•	 The trip duration of casual riders varies a lot where the trip duration of subscribers is more constant.

•	 Both casual riders and subscribers tend to ride more over the weekends.

•	 Both casual riders and subscribers tend to ride longer in the summer and shorter in the winter, but the trip duration of subscribers are more constant than casual riders.

•	 Stations commonly used by casual riders differ from station commonly used by subscribers.


## Recommendation:

Based on my analysis, my recommendation is:

•	Attract casual riders by adjusting the price of membership where it would be cheaper to have annual membership for riders who tend to take longer trips.

•	Run more ad campaigns over the weekends in the app.

•	Give attractive offers for annual memberships right before the beginning of summer.

•	Show more ads on the stations which are used more by the casual riders.


[Notebook and data](https://github.com/Ekram49/Capstone_cyclistic)
