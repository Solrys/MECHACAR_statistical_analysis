# MECHACAR_statistical_analysis
Analysis Using R

## Overview

AUTORSThe purpose of this analysis is to offer insights on the MechaCar's production to help the manufacturing team. In order to conduct this analysis, 

## Method
*Datsets containing information related to the miles per gallon and the suspension coils of the MechaCar. 
*R 
*R studio
*Dyplr Library

## Linear Regression to Predict MPG

First I loaded the miles per gallon dataset. Next I preformed a multiple linear regression to see if it could predict the miles per gallon (mpg) dependent variable by using the vehicle length, vehicle weight, spoiler angle, ground clearance, and all wheel drive (AWD) independent variables. 

### Questions
I wanted to answer three questions:

1) Which variables provided a non-random amount of variance to the mpg values in the dataset?
2) Is the slope of the linear model considered to be zero? 
3) Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

### Answers
1) There were two variables that provided a non-random amount of variance: The vehicle length and the ground_clearance. Both of these have extremely small p-value, in other words that they had a high level of significance. It also should be noted that the intercept as had a high level of significance meaning that there are still other factors contributing to the variance of the miles per gallon of the MechaCar.
The slope of the linear model is not considered to be zero. This is because the linear regression shows that some of the independent variables had a significant effect on the dependent variable. If none of the independent variables had an effect on the dependent variable then the linear regression would result in a near zero slope.
The main indicator of whether the linear model predicts the mpg of the MechaCar is the r-squared value. In this case, it is at 0.7149 mean that out of 100 instances, this model would approximately predict the mpg of the MechaCar correctly 71 times. This means that the model would be considered effective.
Here are the summary results from the linear regression.

### Miles Per Gallon Linear Regression
![linear](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/mpg_linear_regression.png)

### Suspension Coils Analysis
The suspension coils dataset is comprised of 150 different vehicles ID, 3 different lot numbers, and corresponding PSI levels for each vehicle. I therefor created two summary tables to look at the mean, median, variance, and standard deviation of data. The first table looked at of the data as a whole, while the second table looked specific at each of the three different lots that the MechaCars were divided into. 
The Two tables can be seen below:

#### Total Summary
![table1](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/total_sum_sus_coils.png)
#### Lot Summary
![table2](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/lot_sum_sus_coils.png)

#### Questions

#### Answers


