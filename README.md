# Project Overview

## Purpose

The purpose of this project was to perform statistical testing on AutosRUs data in R.  This project performed a linear regression to understand factors impacting fuel efficiency in MechaCar, the newest prototype.  Additionally, suspension coil data was analyzed and various summary statistics were generated to compare to standards.  Finally, a study design was developed for future consideration. 

# Results

## Linear Regression to Predict MPG

The linear regression of the MechaCar_mpg.csv file shows there are factors that are statistically significant to the Miles per Gallon (MPG) dependent variable.  As shown in the results below, the following variables had p-values < 0.05:  vehicle length and ground clearance.  Additionally, the y-intercept had a p-value of < 0.05.  Thus, the evidence supports that these factors have a meaningful impact on MPG values.

The other factors, vehicle weight, spoiler angle, and all wheel drive (AWD), had p-values > 0.05.  Thus, the evidence supports that any impact of these factors upon MPG is not statistically significant.

Since multiple factors were found to be statistically significant, the slope of the line is not considered to be 0.  The data support that the null hypothesis (that the slope of the linear model is 0) is not true.

The r-squared value was 0.71.  This means that our multiple linear regression model approximated the “real world” values about 71% of the time.  

However, since there are only two variables that are supported as being statistically significant, it is possible that our model performs reasonably well with our current dataset but may not perform well with future data.  Before utilizing this linear model to predict future values, it is suggested that additional validation be done to evaluate the level of success with additional data. 

Also, because the y-intercept is statistically significant, there may be other key factors that are not included in the current dataset.  Looking for these factors could help provide a sounder model.  Or, scaling or transforming the vehicle length and/or ground clearance measurements could help improve predictions from the linear model.

![Linear_regression_to_predict_mpg](https://user-images.githubusercontent.com/82730954/128612766-967e5205-0411-4128-bfe6-2c4bac0cbcbf.PNG)

## Summary Statistics on Suspension Coils

The suspension coil data was analyzed.  Summary statistics were generated on the entire dataset.  The table below shows the overall summary in pounds per square inch (PSI).

![Total_summary](https://user-images.githubusercontent.com/82730954/128612774-7fef9ef0-7569-41cd-ba7e-2fa3c69f50a7.PNG)

Additionally, each lot was analyzed separately.  The table below shows the summary statistics for each lot (PSI).

![Lot_summary](https://user-images.githubusercontent.com/82730954/128612779-8bc53148-1cbb-4cd2-9843-e60ecd3385db.PNG)

The design specifications require that suspension coil variance must not exceed 100 lbs. per sq inch (PSI).  

Overall, the coil variance was 62.29 PSI for all lots combined.

When looking at the results by lot, it is noted that the variance for Lot3 fails to meet the design specifications.  **The variance for Lot 3 was 170.29 PSI which exceeds the allowable threshold.**

The variance for Lot 1 and Lot 2 both met the required specification.  Lot 1’s variance was 0.98 and Lot 2’s was 7.47.

## T-Tests on Suspension Coils


### All coils

A t-test was performed to compare the mean of all coils tested in the dataset to the population mean of 1,500 PSI.  As shown in the image below, the p-value was 0.06 which is greater than the significance level of 0.05.  Thus, the evidence supports the null hypothesis.  This supports that the difference seen (the mean of the subjects in our dataset was 1498.78 vs. 1500 in the total population) is attributable to random chance.

![All_coils](https://user-images.githubusercontent.com/82730954/128612792-d17d90f4-7f04-4c5e-89b0-ed49adecba01.PNG)

### Lot 1

Next, a t-test was performed comparing Lot 1 to the overall population.  The resulting p-value, as shown below, was 1.  The mean of Lot 1 and the overall population were both 1500.  Thus, the null hypothesis is supported by the testing.

![Lot1](https://user-images.githubusercontent.com/82730954/128612799-dfb85a8e-a449-4625-820e-f58c7def3f15.PNG)

### Lot 2

Next, a t-test was performed comparing Lot 2 to the overall population.  The p-value, shown below, was 0.61, which supports the null hypothesis.  The testing supports that the difference seen is a result of random chance.

![Lot2](https://user-images.githubusercontent.com/82730954/128612807-df5effba-b175-4ff0-8769-e4ef5ca86dc7.PNG)

### Lot 3

Finally, a t-test was performed comparing Lot 3 to the overall population.  This test, shown below, resulted in a **p-value of 0.04**.  The testing supports that the difference observed between Lot 3 and the population is **not due to random chance and is statistically significant.**  

![Lot3](https://user-images.githubusercontent.com/82730954/128612816-674c17a7-82b4-4361-8802-7b189ecf4752.PNG)

## Study Design:  MechaCar vs Competition

To quantify how MechaCar performs against our competitors, the following study design has been developed.

It is suggested that we evaluate and compare the following factors to compare our vehicles to those of our closest competitors:
* Street price (superior to MSRP which can differ from actual cost)
* Combined fuel economy (per EPA guidelines, weighting the city fuel economy by 55% and the highway fuel economy by 45%)
* Maintenance costs
* Horsepower
* Reliability ratings
* National Highway Traffic Safety Administration (NHTSA) safety ratings
* Design and styling ratings

The null hypothesis is that if there are no differences between all vehicles studied then no statistical variance will be seen in metrics measured.  The alternative hypothesis is that if MechaCars are superior to those of our closest competitors, statistical superiority will be seen in multiple metrics measured.  It is suggested that the significance level be set at 0.05.

After studying and compiling the data, an ANOVA should be performed to determine if statistical differences are observed. Additionally, the metrics should be visualized allowing us to see qualitatively how MechaCars compared to the competition.

It might also be valuable to predetermine a method of developing an index encapsulating all of the above metrics to allow easier comparisons.
