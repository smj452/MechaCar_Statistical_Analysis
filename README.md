# MechaCar Statistical Analysis
In this project R Programming language is used to conduct Statistical modelling, Hypothesis testing and AB testing using a car manufacturing dataset. The different test and their findings are shown below:
## Linear Regression to Predict Miles Per Gallon(MPG)
```MechaCar_mpg.csv``` dataset of 50 car prototypes is used to identify ideal vehicle performance by implementing a multiple linear regression model. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle.
 Using the lm function in R, a linear model that predicts the mpg of the car prototypes using the variables listed above was calculated.

## Summary
![Linear Regression Summary](https://github.com/smj452/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable1_Result2.png)

**Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?**

From the p-values of each variable ```vehicle_length``` and ```ground_clearance``` have a statistically significant influence on the MPG performance of the vehicle. The variation of mpg with the statically significant variables is shown in the screenshot above.

**Is the slope of the linear model considered to be zero? Why or why not?**

The overall low score of the p-values shows that we can reject the null hypothesis which shows that the slope of our linear model is not zero

**Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?**

p-value is below 0.05. Therefore, we have sufficient evidence to reject the null hypothesis. Also, Multiple R-squared values is 0.7149 which means 71.5% of the variance in the mpg can be predicted by all variables. The adjusted R-squared value is 0.6825 which means 68% of the variance in the mpg can be predicted by all variables. Based on the Multiple R-squared, Adjusted R-squared and p-value values linear model predicts mpg of MechaCar prototypes effectively.

## Summary Statistics on Suspension Coils

```Suspension_Coil.csv``` dataset contains the results from multiple production lots. In the dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots.

![Lot Summary](https://github.com/smj452/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable2_Lot_summary.png)

![Total Summary](https://github.com/smj452/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable2_Total_summary.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Based on that specification the current manufacturing data meets this design specification manufacturing lots ```Lot 1``` and ```Lot 2``` but does not meet for ```Lot3``` since the variance of the suspension coils is higher than 100 pounds per square inch.


## T-Tests on Suspension Coils

One-Sample T-Tests were performed to determine if all manufacturing lots and each lot individually are statistically different from the population mean of 1,500 pounds per square inch (PSI).

For this analysis, our hypothesis is as follows:

H0 : There is no statistical difference between the observed sample mean and its presumed population mean.

Ha : There is a statistical difference between the observed sample mean and its presumed population mean.

1. T-Test for all of the manufacturing lots together shows that the p-value of 0.06028 is higher than our significance level of 0.05 and therefore, we do not have sufficient evidence to reject the null hypothesis

![Deliverable 3_T-Test for all of the manufacturing lots.png](https://github.com/smj452/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable%203_T-Test%20for%20all%20of%20the%20manufacturing%20lots.png)

2. T-Test for Lot1 PSI data shows that the p-value of 1 is higher than our significance level of 0.05 and therefore, we do not have sufficient evidence to reject the null hypothesis

![Deliverable3_Result_Lot1.png](https://github.com/smj452/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable3_Result_Lot1.png)

3. T-Test for for Lot2 PSI data show that the p-value of 0.6072 is higher than our significance level of 0.05 and therefore, we do not have sufficient evidence to reject the null hypothesis

![Deliverable3_Result_Lot2.png](https://github.com/smj452/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable3_Result_Lot2.png)

4. Test for all of the manufacturing lots together show that the p-value of 0.04168 is lower than our significance level of 0.05 and therefore we can reject our null hypothesis and conclude that Lot3 sample data is statistically different from the population mean

![Deliverable3_Result_Lot3.png](https://github.com/smj452/MechaCar_Statistical_Analysis/blob/main/Resources/Deliverable3_Result_Lot3.png)


## Study Design: MechaCar vs Competition

The following analysis can be done to determine MechaCar and competitive companies are statistically different. Multiple metrics data for cost, city or highway fuel efficiency, horsepower, maintenance cost, or safety rating, will be collected for each vehicle for MechaCar and its competitors. The following Hypothesis will be tested:

H0: There is no statistical difference between MechaCar and competitive companies.

Ha: There is a statistical difference between MechaCar and competitive companies.

- A two sample t-test can be used to test the hypothesis. The T-test will allow the company to observe if each variable that has a significant difference between MechaCar and competitor companies
- The difference in each variable will help us to conclude if there is a difference in vehicle performance of the MechaCar vehicles against vehicles from its competitors.
- Also Using the t-test, the following metrics: cost, city or highway fuel efficiency, horsepower, maintenance cost, or safety rating will be compared individually for MechaCar and the competitor companies.
