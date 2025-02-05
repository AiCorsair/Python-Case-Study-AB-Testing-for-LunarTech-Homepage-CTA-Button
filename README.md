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


## III. 
