# Project Name
> Multiple Linear Regression model for the prediction of demand for shared bikes


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- This project is to build Multiple linear regression model for predicting the demand of shared bikes 
- A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.
- Boom bikes want to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:
	- Which variables are significant in predicting the demand for shared bikes.
	- How well those variables describe the bike demands
- A dataset has been prepared based on daily bike demands across the American market based on some factors. 

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
- Following are the different steps followed to arive at the Conclusions.
	- Step 1: Data Sourcing
	- Step 2: Data Cleaning
	- Step 3: Data Preparation
	- Step 4: EDA
	- Step-5: Create dummy columns
	- Step6: Splitting Data into Training and Testing Sets
	- Step-7: Model Building
	- Step-8: Residual Analysis of the train data
	- Step-9: Predictions on test data
	
- Following are inferences from EDA
	- Tempearture has positive corellation with demand for bikes
	- There is more demand for bikes in summer and fall seasons
	- Demand for bikes is very less in rainy weather
	- Demand for bikes is less on holiday
	- Weekday and Working day doesnot impact the demand for bikes
	- Demand for bikes increases gradually from jan till july and then it starts decreasing from july till dec
- Following are the conclussions from Multiple Linear
	- Derived the initial model with 15 variables using RFE. R-squared: 0.849
	- Dropped humidity with high VIF(29.40), derived second model with 14 variables. R-squared: 0.843 - Best fit model
	- Dropped temp with VIF(7.07) , derived second model with 13 variables. R-squared: 0.781
	- Drastic decrease in R-squared and Adjusted R-squared after dropping temp. Hence the second model with 14 variables is considered as best model for this dataset.
	- Plotted the error terms Histogram. Its close to normal distribution, Mean value of error terms is almost 0. Hence this model best fit.
	- With best fit model calculated Test data R-squared: 0.805
	- Difference between tarin r-squared and test R-suared is 4.4%. hence this is best fit model
	- Final Model:
	  cnt = 0.1737 + 0.2344 X yr - 0.0562 X holiday + 0.0465 X workingday + 0.4728 X temp - 0.1563 X windspeed - 0.0597 X spring + 0.0434 X summer + 0.0797 X winter + 0.0584 X sat - 0.0826 X cloudy - 0.2917 X rain - 0.0389 X jan - 0.0482 X jul + 0.0753 X Sep



## Technologies Used
- Python - version 3.0
- Pyhton libraries used - pandas, numpy, matplotlib.pyplot, seaborn, sklearn, statsmodels 

## Acknowledgements
Give credit here.
- This project was done as part of Upgrad, IIITB Master of Science in Machine Learning & AI course
- This project was based on [Master of Science in Machine Learning & AI](https://www.upgrad.com/masters-in-ml-ai-ljmu/).


## Contact
Created by [@prakashreddyav] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->