A/B Test Exploratory Analysis
Project Overview
This project focuses on exploring an A/B test to compare the conversion performance of two variants — Control and Treatment.
The analysis was performed using Python and Excel to calculate conversion rates, measure the difference between variants, perform hypothesis testing, and understand whether the observed difference was statistically meaningful.
Objective
The main objectives of this project were to:
Compare conversion rates between Control and Treatment.
Clean and validate the A/B testing data.
Measure the absolute and relative difference in conversion rates.
Perform a statistical hypothesis test.
Calculate the effect size and confidence interval.
Interpret statistical and practical significance.
Provide a business recommendation based on the results.
Dataset
The dataset contains information about users participating in an A/B test.
Columns
Column
Description
user_id
Unique identifier for each user
timestamp
Date and time of the experiment
group
Control or Treatment group
landing_page
Landing page shown to the user
converted
Whether the user converted (0/1)
Data Cleaning
Before performing the analysis, mismatched group and landing-page combinations were removed.
Valid combinations were:
Control → old_page
Treatment → new_page
This ensured that users were correctly assigned to the respective A/B test variants.
After cleaning:
Control users: 145,274
Treatment users: 145,311
Total valid users: 290,585
Conversion Analysis
Metric
Control
Treatment
Total Users
145,274
145,311
Conversions
17,489
17,264
Non-Conversions
127,785
128,047
Conversion Rate
12.04%
11.88%
Effect
Absolute difference: −0.16 percentage points
Relative lift: −1.31%
The Treatment variant had a slightly lower conversion rate than the Control variant.
Hypothesis Testing
Null Hypothesis (H₀)
There is no statistically significant difference between the conversion rates of the Control and Treatment groups.
Alternative Hypothesis (H₁)
There is a statistically significant difference between the conversion rates of the Control and Treatment groups.
Test Used
Two-proportion z-test
Results
Statistical Measure
Result
Z-statistic
≈ 1.31
P-value
≈ 0.19
Significance Level
0.05
Result
Not statistically significant
Since the p-value is greater than 0.05, there is not enough evidence to reject the null hypothesis.
Confidence Interval
The estimated 95% confidence interval for the difference in conversion rates was approximately:
−0.39 to +0.08 percentage points
Since the interval includes zero, the observed difference may be due to normal variation rather than a reliable difference between the variants.
Statistical vs Practical Significance
Statistical significance determines whether the observed difference is likely to be genuine rather than random variation.
Practical significance considers whether the size of the difference is meaningful from a business perspective.
In this analysis:
The result was not statistically significant.
The observed difference was small (−0.16 percentage points).
Therefore, there is no strong evidence that the Treatment variant provides a meaningful improvement.
Business Recommendation
Based on the analysis, the Control variant should be retained.
The Treatment variant had a slightly lower conversion rate, and the difference was not statistically significant. Therefore, there is insufficient evidence to justify replacing the Control variant with Treatment.
Further testing could be considered if there is a strong business reason to investigate the Treatment experience.
Tools Used
Python
Pandas
Excel
Statistical Hypothesis Testing
Key Learnings
Through this project, I practiced:
A/B test data cleaning
Conversion-rate analysis
Hypothesis formulation
Two-proportion z-testing
P-value interpretation
Effect-size calculation
Confidence intervals
Statistical vs practical significance
Translating statistical results into a business recommendation

    └── ab_test_conversion_comparison.png# AB-Test-Exploratory-Analysis
A/B test analysis using Python and Excel to compare conversion rates, perform hypothesis testing, measure effect size, and evaluate statistical significance.
