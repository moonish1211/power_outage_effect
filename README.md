# Power outage Data
<br>
Project created by Jill Luna Nomura

## Introduction
For our society to function, it is an inevitable truth that we must have an adequite power supply to run every businesses and live our daily life. There are many US citizen claiming that having electricity and internet connection to our homes are a basic necessities and are entitled to have these power sources. As covid-19 pandemic changed the livelihood of many people to work virtually from home, we are depending more to these power and if there is any unfortunate circumstances in the future that takes away lights in our home, I argue that the society will be in chaos and confusion. 
<br>
<br>
To make an inference about potential outage in the future, we must first analyze the outage that happened in our nation in the past. We were provided with a dataset from this research paper, **[Data on major power outage events in the continental U.S.](https://www.sciencedirect.com/science/article/pii/S2352340918307182)** under table 1. This data allows us to analyze each outage that happen through US and look at different features such as when, where, cause, and effects of these outage. 

## Framing the Problem

With this dataset, we will utilize **linear regression** to **predict the severity of the outage in terms of the number of customers effected by the outage**
<br>
<br>
The response variable are the number of customers effected by the outage. I chose this variable as a measure of severity of the outage because we saw a negative correlation between the number of customers effected by the outage and the duration of the outage, through the scatter plot. 
<br>
The visualization is posted here
<iframe src="assets/duration_effected_customer.html" width=600 height=600 frameBorder=0></iframe>
<br>
This means that as more customer effected, the faster the company deals with the issue to resolution. If we can predict how many customers are effected in the outage, we can immediately prioritize certain cases over others, which can lead to faster correspondence in the future outage. 
<br>
<br>
We chose the metric RMSE to evaluate this model because I argue that more distance between the prediction and the actual value should be punished with more error and RMSE clearly reflect this concerns. By squaring the distance between the predicted and actual value, the more the prediction is off equavalate to more error and that is what we are more concerned with than using other metrics like coefficient of determination which measure the quality of a linear fit.

## Baseline Model
The model that were used is the LinearRegression Model with two features, POSTAL.CODE and OUTAGE.DURATION(hr).
Since there were some missing value in the CUSTOMERS.AFFECTED column, I decided to delete these rows instead of imputation. This is because I didn't want to alter the variability of the score and make the prediction bias. I ended up deleting 500 rows from the dataframe. 

The POSTAL.CODE is a nominal data, so I performed a One Hot Encoding to this column. My OUTAGE.DURATION(hr) is a quantitative data, so I decide to leave this as is for my baseline model. 

The performance of my model turned out to have a RMSE on training data as 254796.81565928235 and the RMSE of test data as 331371.2375319377. Although this RMSE depends on the train test split I do to the original dataframe, but we can see that there this model is overfitting to the DGP. This model was good in a way that it was simple for using minimum number of column to fit this model, but this the fact that this model overfitts shows that there needs to be an improvement to be done. 

## Final Model

## Fairness Analysis