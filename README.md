# bike-sharing-system

Bike sharing system is an innovative transportation strategy that provides individuals with bikes for their common use on a short-term basis for a price or for free. Over the last few decades, there has been a significant increase in the popularity of bike-sharing systems all over the world. This is because it is an environmentally sustainable, convenient and economical way of improving urban mobility. In addition to this, this system also helps to promote healthier habits among its users and reduce fuel consumption.


🎯 The goals of this project are:

Understand the trends in the data and identify key factors affecting the hourly demand for rental bikes.

Build an appropriate regression model to forecast the number of rental bikes required per hour.

#### Problem Statement
To predict demand of bike rental for this program

Each row of data represents a bike demand under the given for the given attrubutes and each column contains represents the attributes.

dteday : Date

Season : Season of the year

yr : we have data for two years, so this represents the year to which the specific data belongs to

mnth : Month of the Year

hr : Time/Hour of the day (24 hours format)

yr : Whether the day was a holiday

weekday : Day of the week

workingday : Whether the day was a working day or a holiday

weathersit , temp , atemp , hum , windspeed : Weather conditions for the day

casual , registered : Non-Registered and registered users

cnt : total count/demand for the particular condition on the date


## Approach

+ Loading Data
	- Renaming attributes
	- Performing type casting

+ Data Exploration and Visualization
	
+ Spliting Data for Train and test

+ Data Preprocessing
    
	- Label Encoding 

	- One Hot Encoding of Categorical Values

+ Training Model

	- Linear Regression
	- Decision Tree

In order to measure the performance of the model, Mean Squared Error and R-square for the model is used.


## Data Exploration and Visualization

__Data Info__

![](Images/Data%20Description.PNG)

__Data Distribution__

![](Images/Exploratory%20Data%20Analysis.PNG)

__Seasonwise Demand__

![](Images/Seasonwise%20Distribution.PNG)

__Daily Hourly Distribution of Demand__

![](Images/Hourly%20Distribution.PNG)

__Monthly Distribution of Demand__

![](Images/Monthly%20Distribution.PNG)

__Year Wise Demand__

![](Images/Yearwise.PNG)

__Demand for Registered users and weather conditions__

![](Images/registered%20and%20weather.PNG)

__Outlier for Demand Hourswise__

![](Images/Demand%20Across%20hour.PNG)

__Working day and Holiday Demand Distribution__

![](Images/Working%20Day%20vs%20Holiday.PNG)

__Correlation Heat Map of All Features__

![](Images/Correlation%20Heatmap.PNG)


## Model Building and Training

1. ### __Linear Regression__

    __Training Data__

    Cross validation

    __R-squared__::[0.26906982 0.22635143 0.26170837 0.25691577 0.32148609 0.31196355 0.26400442 0.28760857 0.27964318 0.31554976]

    __MSE__ :: [-23850.18552648 -24978.92079695 -24408.88562232 -22517.19952749 -22117.37661082 -24746.90893471 -25327.37663767 -25328.57026724 -25094.24038362 -21876.91293786]


    __Testing Model__

    __R-squared__ ::0.2867680055878652

    __MSE__: 22753.14

2. ### __Decision Tree Model__

    __Training Data__
    
    Grid search with Cross validation

    __R-Squared__::0.29472840660973104

    __Best Hyperparameters__::{'criterion': 'mse', 'max_depth': 8, 'max_leaf_nodes': 500, 'min_samples_leaf': 20, 'min_samples_split': 5}

    __Avg R-squared__::0.30744642968000135

    __MSE__::-23089.90043082429



    __Testing Model__

    __R-squared__::0.3238351376141839

    __MSE__: 21570.64

    ## Conclusion
From the Model Comparison we see that Decision Tree Model has higher R-squared value and lower Mean Square Error over the Linear Regressioni Model. Hence it is more favourable, however we can experiment further with more algorithms to have even a better R-square and lower MSE.
