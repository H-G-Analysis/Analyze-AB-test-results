# Analyze A/B test results
## by (Hadeer Ismail Gado)


## Introduction

>Our project is concerned of analyzing results of an A/B test run by an e-commerce website. Our goal is to help the company understand if they should implement the new page, keep the old page, or perhaps run the experiment longer to make their decision.

## Project Walkthrough

>Our project is divided into 3 parts:
>Part 1 - Probability:
  >By applying Probability on the dataset, we found that the probability of Individual converting is 12%. The Probability of individual receiving new page is 50%. Although the convertion rate in control group is greater than the convertion rate in treatment group but the difference is nearly approximate. Still there is no strong evidence to conclude that the new treatment page leads to more conversions, so in the next part we will use Hypothesis testing.

>part 2 - A/B Test:
  >In this part we will apply hypothesis testing on our dataset. we ended up with p-value which is "the probability of obtaining the data or more extreme values from the null hypothesis". And the result was 0.9,which is greater than alpha. Then based on this result We fail to reject the Null.
  >We stay with the Null hypothesis. which means that the Old page is better than or equal in convertion rate than the new page.

>part 3 - Regression Approach:
  >Our response variable is categorical, so it is better to use Logistic regression as we are predicting only two possible outcome( conversion or no conversion).
  >After applying regression model we got p_value equal to 0.19, which is different from p_value in part 2. In part 3 we were predicting convertion in new page, which is two-tailed test. I divide the alpha into two parts, half of the alpha for testing in one direction and the other half for testing in the other direction. But in part 2 it was a one-tailed test, so it means alpha is for the one direction test. we assumed the null Hypothesis as old page has higher conversion rate than new page or the same, so p-value is compared with this test.


## Summary of Findings

>A/B data shows the data for convertion either for experiment/treatment user who experience the new page or the control user who use old page. Our first analysis shows that the proportion of user who converted in control group was 12%, on the other hand the proportion of user who converted in the treatment group was 11.9%.The convertion rate in both group is nearly approximate. keeping in mind the probability of user who received new page was 0.5.
>In Hypothesis testing by default we assume the null is true. We assume that the old page is better unless the new page proves to be definitely better at a Type I error rate of 5%. In hypothesis test we got a p-value equal to 0.9, based on this result We fail to reject the Null.
>Our response variable is categorical, so we used Logistic regression as we are predicting only two possible outcome( conversion or no conversion).In our first model we were predicting convertion in new page. So we got p-value of 0.19 which was different from p-value in the previous hypothesis part. In the second model we predicted conversion rate based on country of user, Differences in values between countries based on conversion rate are approximate to 1, so there is no preferences in country.

## Conclusion

>Based on these different tests, we recommend to stay with old page or make more improvement to enhance convertion rate
