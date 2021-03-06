# MECHACAR_statistical_analysis
Analysis Using R

## Overview

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on me to review the production data for insights that may help the manufacturing team.

I will be doing the following:
* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.


## Method
* Datsets containing information related to the miles per gallon and the suspension coils of the MechaCar. 

* R 

* R studio

* Dyplr Library

## Linear Regression to Predict MPG

First I loaded the miles per gallon dataset. Next I preformed a multiple linear regression to see if it could predict the miles per gallon (mpg) dependent variable by using the vehicle length, vehicle weight, spoiler angle, ground clearance, and all wheel drive (AWD) independent variables.

## Hypothesis

* Null: The slope of the linear model is zero.
* Alternative Hypothesis: The slope of the linear model is not zero.

### Questions:
I wanted to answer three questions:

1) Which variables provided a non-random amount of variance to the mpg values in the dataset?
2) Is the slope of the linear model considered to be zero? 
3) Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

### Results:
1) There were two variables that provided a non-random amount of variance: The vehicle length and the ground_clearance. Both of these have extremely small p-value, in other words that they had a high level of significance. It also should be noted that the intercept as had a high level of significance meaning that there are still other factors contributing to the variance of the miles per gallon of the MechaCar.
The slope of the linear model is not considered to be zero. This is because the linear regression shows that some of the independent variables had a significant effect on the dependent variable. If none of the independent variables had an effect on the dependent variable then the linear regression would result in a near zero slope.
The main indicator of whether the linear model predicts the mpg of the MechaCar is the r-squared value. In this case, it is at 0.7149 mean that out of 100 instances, this model would approximately predict the mpg of the MechaCar correctly 71 times. This means that the model would be considered effective.
Here are the summary results from the linear regression.

### Miles Per Gallon Linear Regression
![linear](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/mpg_linear_regression.png)

### Suspension Coils Analysis
The suspension coils dataset is comprised of 150 different vehicles ID, 3 different lot numbers, and corresponding PSI levels for each vehicle. I therefor created two summary tables to look at the mean, median, variance, and standard deviation of data. The first table looked at of the data as a whole, while the second table looked specific at each of the three different lots that the MechaCars were divided into. 

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

### Results

The Two tables can be seen below:

#### Total Summary
![table1](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/total_sum_sus_coils.png)
#### Lot Summary
![table2](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/lot_sum_sus_coils.png)


Looking at the total summary, the current variance is approximately 76.23 PSI meaning that is does meet the design specification. When looking at the lots individuals, the first two lotas meet the design specification at a varaince of approximately 1.14 PSI and 10.13 PSI respectfully, but the third lot does not. This is becasue the third lot's variance is approximately 220.01 PSI, exceeding the design specification by more than double the alotted amount. Therefore, the manufacturing team should work with the cars in lots 1 and 2 compared to those in lot 3.

### T Test/ Suspension Coils
In this section, I wanted to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch. In order to do this, I used R's t.test() function to find four different p-values. 
#### Question: 
Do any of the four groups have a statistically different mean from the population mena of 1,500 PSI?

#### Hypothesis
* Null: There’s no statistical differences between the observed sample mean and its presumed population mean.
* Alternative: There’s a statistical difference between the observed sample mean and its presumed population mean.

#### Results:
Here is a breakdown of each of the four tests:

![test1](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/total_pop_test.png)
![test 2](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/1_pop_test.png)
![test 3](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/2_pop_test.png)
![test 4](https://github.com/Solrys/MECHACAR_statistical_analysis/blob/main/images/3_pop_test.png)

By using a significance level of 95%, meaning that 95% of the time this tests results would be true, I tested to see if any of the four groups had a statistical difference from the mean of 1,500 PSI. After running the tests, all four p-values where much greater than .05 meaning that I would fail to reject that there is a statistical difference between the four groups and the population mean.


### Final Analysis
### Mechacar VS Competion

For the final section on this study, I will comprise a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.
The following questions and answers will help provide structure for the comparison.

## Questions: 
What metric or metrics will be tested?
What is the null hypothesis or alternative hypothesis?
What statistical tests could be used to test the hypothesis? And why?
What data is needed to run the statistical test?

## Future Analysis:
The metrics I want to test are city and highway fuel efficiencies.
Null Hypothesis is that all of the cars in the same class have the same fuel efficienies. The Alternative Hypothesis is that they are not all the same.
I would use an ANOVA test to complete this analysis for both types of fuel efficiencies. Also I would use the ggplot2 library to show the potential spread between different cars using a boxplot.
I would need fuel efficiency data from 50 individual cars to create a sample size of data for each car in the class type. For example, if there was 10 cars in the class type, I would have a top of 500 data points collected for each fuel efficiency type.
