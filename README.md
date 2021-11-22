# MechaCar_Statistical_Analysis

Jeremy has been approached to review production data for the new MechaCar
Jermey has been asked to preform regression analysis to identify:
1) which variables that predict mpg
2) collect summary statistics  on PSI of the suspension coils from manufacturing lots
3) run t-tests to determine if the manfacturing lots are statistically different from general population
4) Finally, design a statistical study to compare vehicle performance for the MechaCar against competitive vehicles


Linear Regression
please see the resource file for images
The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle.
<img width="510" alt="2021-11-21 (6)" src="https://user-images.githubusercontent.com/86638388/142790854-85688611-5272-4df0-a116-3992e234bc42.png">
In this distribution of the residuals, the dataset fits in with the normal parameters, where the absolute value of the min and max are comparable |-19.47|~|18.58| and the median -.07 is close to zero.

<img width="505" alt="2021-11-21 (5)" src="https://user-images.githubusercontent.com/86638388/142790973-70dbb6aa-7c97-40f0-acd6-e9af12a1348e.png">

The multiple linear regression formula for mpg = -.01 + 6.267(vehicle length)+.001(vehicle weight)+.069(spoiler angle)+3.546(ground clearance)-3.411(AWD), which results in a non-zero slope.

Does this linear model predict mpg?  The R-squared is .7149, which shows strong correlation for the dataset and shows the dataset is an valid. However, r-squared is not the only consideration for effectiveness. There could be other variables not included in the dataset contributing to the variation in the mpg.


Visualizations for Trip Analysis
The dataset contains the results from multiple production lots. In the dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots
A summary is required to understand:
The suspension coil’s PSI continuous variable across all manufacturing lots
The following PSI metrics for each lot: mean, median, variance, and standard deviation.

<img width="342" alt="2021-11-21 (2)" src="https://user-images.githubusercontent.com/86638388/142791815-4a31c5dd-f73c-4835-b16b-ebd9b17d88d1.png">

<img width="487" alt="2021-11-21 (3)" src="https://user-images.githubusercontent.com/86638388/142791833-5e045ec8-09a8-4a42-b2bb-ca63ad54d8fc.png">

The variance for the total manufacturing lot is 62 < 100, which is within the expected specifications of staying under 100 PSI. However, when reviewing the data by Lot number, Lot 3 is a large contributing factor to the variance being high. Lot 3 shows a variance of 170 > 100 and therefore does not meet the design specifications. Lot 1 and Lot 2 have significantly lower variance, 1 and 7 respectively.

T-Tests on Suspension Coils
All Manufacturing Lots: p-value = .6028, alpha = .05
.60 > .05, which means the total manufacturing lot is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.
<img width="487" alt="2021-11-21 (7)" src="https://user-images.githubusercontent.com/86638388/142792615-dea5c234-d66f-4822-9d93-ebd6935944d5.png">

T-test for Lot 1
Lot 1: p-value = 1, alpha = .05
1 > .05, which means Lot 1 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.
<img width="502" alt="2021-11-21 (8)" src="https://user-images.githubusercontent.com/86638388/142792616-7483f7d1-9473-4484-a715-0fb006f2eb02.png">

T-test for Lot 2
Lot 2: p-value = .6072, alpha = .05
.60 > .05, which means Lot 2 is not statistically significant from the normal distribution and normality can be assumed. The mean falls within the 95% confidence interval.
<img width="510" alt="2021-11-21 (9)" src="https://user-images.githubusercontent.com/86638388/142792617-2704755a-bcb5-4eea-8e4b-427a54bdb7e7.png">

T-test for Lot 3
Lot 3: p-value = .04168, alpha = .05
.04 < .05, which means it is statistically significant from the normal distribution and normality cannot be assumed. However, the mean falls within the 95% confidence interval.
<img width="381" alt="2021-11-21 (10)" src="https://user-images.githubusercontent.com/86638388/142792618-1c7e1cdc-1d4f-4bac-9049-190aa860aca0.png">

The overall manufacturing, Lot 1, and Lot 2 show a normal distribution. Therefore, there is not sufficient evidence to reject the null hypothesis, which shows the two means are statistically similar.


Study Design: MechaCar vs Competition

When comparing MechaCar to its competitor’s other metrics that could be of interest to a consumer could include cost, real fuel efficiency, maintenance cost, or safety rating.

What metric or metrics are you going to test?
The next metrics to test should be the safety rating, horsepower, and fuel efficiency, which address some safety concerns of consumers.

What is the null hypothesis or alternative hypothesis?
The null hypothesis is that the mean of the safety rating is zero. The alternative hypothesis is that the mean of the safety rating is not zero.

What statistical test would you use to test the hypothesis? And why?
Using a multiple linear regression statistical summary would show how the variables impact the safety ratings for MechaCar and their competitors.

What data is needed to run the statistical test?
A random sample of n > 30 for MechaCar and their competitor, would need to be collected including the safety ratings, highway fuel efficiency, and horsepower plus running the data through RStudio.

