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
The response variable are the number of customers effected by the outage. I chose this variable as a measure of severity of the outage because when we visualize the relationship between the number of customers effected by the outage and the duration of the outage, we saw a negative correlation between this variable. This means that as more customer effected, the faster the company deals with the issue to resolution. If we can predict how many customers are effected in the outage, we can immediately prioritize certain cases over others, which can lead to faster prevention in the future outage. 
The visualization is below
<iframe src="assets/duration_effected_customer.html" width=800 height=600 frameBorder=0></iframe>

## Baseline Model

## Final Model

## Fairness Analysis