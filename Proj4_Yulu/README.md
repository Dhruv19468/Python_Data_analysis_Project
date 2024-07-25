![R](https://github.com/user-attachments/assets/e081e939-8695-43d4-8ff8-a3d024c7923f)


# About The Case Study

### Problem statement:
* Strategic Expansion: Yulu's decision to enter the Indian market is a strategic move to
expand its global footprint. Understanding the demand factors in this new market is
essential to tailor their services and strategies accordingly.
* Revenue Recovery: Yulu's recent revenue decline is a pressing concern. By analyzing the
factors affecting demand for shared electric cycles in the Indian market, they can make
informed adjustments to regain profitability.


Column Profiling:
* datetime: datetime
* season: season (1: spring, 2: summer, 3: fall, 4: winter)
* holiday : whether day is a holiday or not
* workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
* weather:
  * Clear, Few clouds, partly cloudy
  * Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
  * Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
  * Heavy Rain + Ice Pellets + Thunderstorm + Mist, Snow + Fog
* temp: temperature in Celsius
* atemp: feeling temperature in Celsius
* humidity: humidity
* windspeed: wind speed
* casual: count of casual users
* registered: count of registered users
* count: count of total rental bikes including both casual and registered


#### Analysis on the Data set has been executed on the Jupyter notebook.



## Work Flow on Data Set

______________________________________________________________________________
##### 1. Define the Problem Statement, Import the required Libraries and perform Exploratory Data Analysis.
* Examine dataset structure, characteristics, and statistical summary.
* Identify missing values and perform Imputation using an appropriate method.
* Identify and remove duplicate records.
* Analyze the distribution of Numerical & Categorical variables, separately
* Check for Outliers and deal with them accordingly.

______________________________________________________________________________
##### 2. Try establishing a Relationship between the Dependent and Independent Variables.

______________________________________________________________________________
##### 3. Check if there any significant difference between the no. of bike rides on Weekdays and Weekends?
* Formulate Null Hypothesis (H0) and Alternate Hypothesis (H1)
* Select an appropriate test
* Set a significance level
* Calculate test Statistics / p-value
* Decide whether to accept or reject the Null Hypothesis.
* Draw inferences & conclusions from the analysis and provide recommendations.
  
______________________________________________________________________________
##### 4. Check if the demand of bicycles on rent is the same for different Weather conditions?
* Formulate Null Hypothesis (H0) and Alternate Hypothesis (H1)
* Select an appropriate test
* Check assumptions of the test
  * Normality
  * Equality Variance
  * Please continue doing the analysis even if some assumptions fail
* Set a significance level and Calculate the test Statistics / p-value.
* Decide whether to accept or reject the Null Hypothesis.
* Draw inferences & conclusions from the analysis and provide recommendations.

______________________________________________________________________________
##### 5. Check if the demand of bicycles on rent is the same for different Seasons?
* Formulate Null Hypothesis (H0) and Alternate Hypothesis (H1)
* Select an appropriate test -
* Check assumptions of the test
  * Normality
  * Equality Variance
  * Please continue doing the analysis even if some assumptions fail
* Set a significance level and Calculate the test Statistics / p-value.
* Decide whether to accept or reject the Null Hypothesis
* Draw inferences & conclusions from the analysis and provide recommendations.

______________________________________________________________________________
##### 6. Check if the Weather conditions are significantly different during different Seasons?
* Formulate Null Hypothesis (H0) and Alternate Hypothesis (H1) distinct Categories. Encode them accordingly.
* Select an appropriate test
* Create a Contingency Table against ‘Weather’ & ‘Season’ columns
* Set a significance level and Calculate the test Statistics / p-value.
* Decide whether to accept or reject the Null Hypothesis.
* Draw inferences & conclusions from the analysis and provide recommendations.


Recommendation and insights of the data analysis has been added in the PDF.


