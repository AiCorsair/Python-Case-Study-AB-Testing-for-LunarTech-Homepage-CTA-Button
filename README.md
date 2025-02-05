# Python Case Study: A/B Testing for LunarTech Homepage's CTA Button


## Table of Contents
- [I. Introduction](#I.-Introduction)
- [II. Hypotheses & Dataset Overview](#II.-Hypotheses-&-Dataset-Overview)
- [III. Key Steps](#III.-Key-Steps)
- [IV. Key Visualizations](#IV.-Key-Visualizations)
- [V. Key Explanations](#V.-Key-Explanations)
- [VI. Conclusion](#VI.-Conclusion)


## I. Introduction

In this project, we conducted an A/B test for LunarTech using proxy data structured similarly to the company's real data. LunarTech is a platform offering courses, bootcamps, and career support to help students land their ideal data role.

A/B testing is a widely used statistical method for comparing two versions of a variable. In this case, we aimed to identify which version of LunarTech homepage’s CTA button performs better based on the click-through rate (CTR) metric:

- **Control Group:** Exposed to the current CTA button ("Secure Free Trial").

- **Experimental Group:** Exposed to the new, generalized CTA button ("Enroll Now").

Click-Through Rate (CTR) measures the percentage of users who click a button or link after viewing it. For LunarTech, CTR is important because it reflects user engagement with the platform and helps assess the effectiveness of call-to-action buttons in driving sign-ups and conversions.

Finally, the results of this test will help decide whether to implement the new button on LunarTech’s homepage.


## II. Hypotheses & Dataset Overview

Here are the statistical hypotheses we made:

- **Null Hypothesis (H₀):** There exists no statistically significant difference in CTR between the experimental ("Enroll Now") and control ("Secure Free Trial") buttons on the homepage.

- **Alternative Hypothesis (H₁):** There exists a statistically significant difference in CTR between the experimental and control buttons on the homepage.

We used a sufficiently large, random sample to ensure the results represent the entire user population, enabling confident business decisions. Below are the columns in the dataset:

- **user_id:** Unique identifier for users (`1` to `20,000`).

- **click:** `1` if the user clicked the CTA button, `0` if not.

- **group:** Either "con" (control) or "exp" (experimental), with an even split.

- **timestamp:** Click date and time for the "exp" group (Jan `1-7`, `2024`) at minute-level precision.


## III. Key Steps

- We imported the necessary libraries and loaded the dataset from a CSV file.

- We explored the data using summary statistics, plotted total clicks and non-clicks for each group, and annotated bars with click and non-click percentages.

- We set the significance level at `α = 0.05` to control Type I errors (false positives) and the minimum detectable effect at `δ = 0.1`, as the business required at least a `10%` CTR increase to justify implementation.

- We calculated total users and clicks per group, estimated click probabilities, pooled click probability, and pooled click variance.

- We determined the standard error, Z-statistic, and Z-critical value, then assessed statistical significance using the p-value and a standard normal distribution plot.

- Finally, we checked practical significance using a `95%` confidence interval.


## IV. Key Visualizations

![Total Clicks](https://github.com/user-attachments/assets/bda8fc17-008b-4684-a16d-c1d36bbdef7d)

As shown, `61.16%` of users clicked in the experimental group, compared to only `19.89%` in the control group. Hypothesis testing confirmed that this difference is statistically significant and not due to chance.

![Statistical Significance](https://github.com/user-attachments/assets/afef3345-1460-4eac-ac7e-5fc637fc0cf2)

The graph shows the standard normal distribution with a mean of `0` and a standard deviation of `1`. The rejection regions are located before and after the Z-critical values of `-1.96` and `1.96`, respectively. Since the Z-statistic is `-59.44`, well beyond the critical value of `-1.96`, we rejected the null hypothesis.


## V. Key Explanations

