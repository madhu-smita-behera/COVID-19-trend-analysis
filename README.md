# COVID-19-trend-analysis
## Problem Statement

The COVID-19 pandemic has swept across the globe, impacting lives, healthcare systems, economies, and societies at an unprecedented scale. Amidst the crisis, there is a critical need to comprehensively analyze the trends associated with the pandemic to 

	Understand the dynamics
	Identity risk factors and vulnerabilities
	Assess the efficacy of interventions
	Predictive modeling
	Inform policy and decision-making

This analysis will involve analyzing vast datasets having epidemiological, clinical, and intervention-related information. Utilizing advanced statistical and machine learning techniques, this research aims to uncover patterns, correlations, and casual relationships within data to guide effective strategies in controlling and managing the COVID-19 pandemic.

The ultimate goal is to leverage data-driven insights to mitigate the spread of the virus, minimize its impact on public health and societal well-being, and facilitate the development of sustainable strategies for future pandemic preparedness and response. 

## Data Description
The dataset available is ‘covid19dataset.csv’, which contains 49068 records and 19 features. 


The features are:
1. PROVINCE / STATE: state name
2. COUNTRY / REGION: country name
3. LAT: latitude of the location
4. LONG: longitude of the location
5. DATE: date of the record
6. CONFIRMED: confirmed cases on that day at that location
7. DEATHS: number of deaths on that day
8. RECOVERED: number of recovered cases on that day
9. ACTIVE: number of active cases on that day
10. WHO REGION: which WHO region does that place belong

There are 34404 missing values in the state/province column of the dataset.

## Data Preprocessing Steps and Inspiration
The preprocessing of the data included the following steps:

1.	First, rename the columns for easy access.
2.	There are missing values present in the state column but our approach for this project relies on country data. So, it's fine to ignore the presence of missing values in the state column.
3.	Change the datatype of the date column from object to datetime.
4.	Visualize the most active countries on the last day of the dataset (plot a world map through choropleth).
5.	Visualize the trend of confirmed cases in the dataset.
6.	Visualize the top 20 active countries on the last given day based on
	Active cases
	Deaths
	Recovered cases, and find out which countries fall in the top 5 or top 3. Further visualizations will be based on these top few countries.
7.	Check the trend of confirmed, active, death, and recovered in selected countries.

## Choosing the Algorithm for the Project
FBProphet:
Prophet is a procedure for forecasting time series data based on an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend and typically handles outliers well.
Some advantages of a prophet are:
•	Accurate and fast
•	Fully automatic
•	Tunable forecasts
•	Available in R or Python


I have chosen the FBProphet algorithm for this project for the following reasons:

1.	The COVID-19 dataset contains lots of missing values. Prophet is designed to require minimal data pre-processing. Thus, it can handle missing data and outliers very well.
2.	This algorithm requires domain knowledge and human input for information related to external factors such as lockdowns, vaccines, etc. So, it requires flexibility to do so.
3.	COVID-19 trends often exhibit seasonality or changing patterns due to many factors such as waves of infection, the beginning of lockdown, etc. Prophet’s ability to capture these seasonality trends makes it a good choice. 
4.	Prophet is scalable and handles large datasets well. This is necessary while analyzing pandemic trends. 
5.	Prophet’s forecasting abilities are valuable for predicting future COVID-19 trends, aiding in resource planning, and decision-making for public health interventions and medical resource allocation. 




