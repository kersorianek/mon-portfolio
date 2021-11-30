---
layout: post
title: Fishing predictor
subtitle:A web app to predict fishing activity of vessels
image: https://eco-business.imgix.net/uploads/ebmedia/fileuploads/shutterstock_126712838.jpg?fit=crop&h=960&ixlib=django-1.2.0&w=1440
---

This web app is built to predict fishing activity of Pole and Line vessels using the vessels position,
speed and the time of the year. The data was collected from “Global Fishing Watch” – a non-profit 
that does scientific research using data and analysis to make fishing activity more sustainable.



![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/map%20of%20fishing.png)



## Data analysis and Feature Engineering

The dataset has various features like 'Longitude', 'Latitude', 'Speed' etc which is used to predict 
the vessels fishing activity.



![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/Features.png)



Features like speed, distance from port, Longitude and Latitude was taken directly from the data. 
The feature “Area” as created from calculating Longitude and Latitude, and Month was extracted from 
Timestamp data.



![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/Area.png)



## Predictive Model

For prediction “Random Forest Classifier” model was used since it is suitable for both numerical and 
categorical variables.



![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/Model.png)



## Model accuracy and Precision

After running and testing the model it was found that the model had a test score of 96%, which is a 
pretty good score. But since the data was imbalanced, I decided that a high accuracy score may not be 
a good metric for the model. So, I also checked precision, recall and f1 score of the model. All of 
them had scored over 90%.



![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/Confusion%20Matrix.png)
![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/Classification%20report.png)



## Web app

Finally, I created a web app using Heroku and integrated the model. Now anyone can with the necessary 
information can use the app to predict fishing activity.



![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/Prediction%20page.png)


![Crepe](https://raw.githubusercontent.com/Ekram49/gfw/master/Images/Result.png)



## Future plan for the project

I’m really proud of being able to complete this whole project by myself. The app is perfectly working 
as planned, but I believe there is always room for improvement. Some of the things I might try in the 
future includes:

1.	Tune the parameters of the model for better accuracy/precision
2.	Try different predictive models.
3.	Try to create and use new features


[Notebook and data](https://github.com/Ekram49/gfw)
