# MechaCar Statistical Analysis

## Overview of the Analysis
 The MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. The data analytics team was asked to review the production data for insights that may help the manufacturing team. A study design proposal was also generated to compare vehicle performance of MechaCar vehicles against vehicles from other manufacturers. The following tests were performed to generate insights:
 - Multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes.
 - Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
 - Run t-tests to determine if the manufacturing lots are statistically different from the mean population.


## Linear Regression to Predict MPG

![Linear Regression](https://github.com/kntln/MechaCar_Statistical_Analysis/blob/main/figures/Linear_Regression.png)

1. Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    -   Based on the analysis, vehicle length and ground clearance are statistically unlikely to provide random amounts of variance to the mpg in the data set. This means that vehicle length and ground clearance have a significant impact on mpg on MechaCar.
2. Is the slope of the linear model considered to be zero? Why or why not?
    - The analysis yielded a p-value of 5.35e-11. Therefore, we can state that there is sufficient evidence to reject the null hypothesis, which means that the slope of our linear model is not zero. 
3. Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
    - From the linear regression model, the r-squared value is 0.71, which means that roughly 71% of the variablilty of the dependent variable (miles per gallon) is explained using this linear model. Hence, the linear model effectively predicts mpg of MechaCar prototypes.

## Summary Statistics on Suspension Coils

![Total Summary](https://github.com/kntln/MechaCar_Statistical_Analysis/blob/main/figures/Total_Summary.png)

![Lot Summary](https://github.com/kntln/MechaCar_Statistical_Analysis/blob/main/figures/Lot_Summary.png)

1. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
    - The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Looking at all manufacturing lots, the variance is 62.29 which meets the 100 PSI requirement. However, upon further investigation of each manufacturing lot, lot 1 generated 0.98 variance, lot 2 generated 7.47 variance, while lot 3 generated 170.29 variance. Therefore, lot 1 and 2 meet the design specifications and lot 3 does not. 

## T-Tests on Suspension Coils
1. Total Manufacturing Lots
    - T-test was used to determine if the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch. The test yielded a p-value of 0.06 which is above the common 0.05 percent significance level. Hence, there is no sufficient evidence to reject the null hypothesis, and the mean of all three manufacturing lots is not statistically different to the population mean of 1500.

![Total Summary t-test](https://github.com/kntln/MechaCar_Statistical_Analysis/blob/main/figures/total_summary_ttest.png)

2. Individual Lots
    - The t-test for Lot 1 generated a p-value = 1 which is higher than 0.05 siginificance level. Therefore, we fail to reject the null hypothesis and Lot 1 not statistically different to the population mean of 1500.![Lot 1 t-test](https://github.com/kntln/MechaCar_Statistical_Analysis/blob/main/figures/lot1_ttest.png)
    - The p-value of Lot 2 is equals to 0.61. Similar to Lot 1, we fail to reject the null hypothesis and therefore it can be concluded that Lot 2 is statistically similar to the population mean of 1500.
    ![Lot 2 t-test](https://github.com/kntln/MechaCar_Statistical_Analysis/blob/main/figures/lot2_ttest.png)
    - Lot 3 yielded a p-value of 0.04 which is lower than 0.05 significance level. In this case, there is sufficient evidence to reject the null hypothesis. Thus, Lot 3 is statistically different from the population mean of 1500. Further investigation on Lot 3's production is warranted as this could be impeding with the progress of the manufacturing team of MechaCar.
    ![Lot 3 t-test](https://github.com/kntln/MechaCar_Statistical_Analysis/blob/main/figures/lot3_ttest.png)


## Study Design: MechaCar vs Competition
What makes a car stand out from its competition? Different factors are involved when it comes to answering that question. Therefore, the purpose of this study design is to quantify how the MechaCar performs against its competition. 

1. What metric or metrics are you going to test?
- For this study design, the metrics that will be tested are as follows: price, fuel efficiency and safety rating.  

2. What is the null hypothesis or alternative hypothesis?
- Null Hypothesis (Ho): There is no statistical difference in terms of price, fuel efficiency and safety rating between MechaCar and its competition. 
- Alternative Hypothesis (Ha): MechaCar is statistically different from its competition in at least one of the following factors: price, fuel economy and safety rating.

3. What statistical test would you use to test the hypothesis? And why?
- The statistical analysis that would be used to test the hypothesis is one-way ANOVA. This is because ANOVA is the most efficient way to compare means across more than two samples or groups. 

4. What data is needed to run the statistical test?
- Price, fuel efficiency and safety rating will be collected from MechaCar and from at least 5 other manufacturers that has a car style comparable to MechaCar.