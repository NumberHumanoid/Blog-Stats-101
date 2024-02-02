# The Ultimate Cheat Sheet for Advanced Data Science Statistics

![banner1](https://github.com/NumberHumanoid/Stats-101/assets/149428916/09eb1a51-6733-41e0-9d36-c15e04b06fc8)


# Unlocking Insights Through Data Analytics Across Industries

Diving into the realm of data analytics can feel like unlocking a treasure trove of insights that drive strategic decisions across various fields. From HR to marketing, and even niche sectors you might not immediately think of, analytics play a pivotal role in deciphering the story behind the data. Let's kick things off with a quick tour of how analytics shape different industries:

- ## People Analytics
  - **Objective**: Harnessing workforce data to improve recruitment, retention, and employee satisfaction.
  - **Toolkit**: Regression analysis for predicting employee turnover and sentiment analysis for gauging employee engagement.

- ## Marketing Analytics
  - **Objective**: Understanding consumer behavior to enhance marketing strategies.
  - **Toolkit**: A/B testing, cluster analysis for market segmentation, and predictive modeling to forecast sales trends.

- ## Healthcare Analytics
  - **Objective**: Improving patient outcomes and healthcare resource management.
  - **Toolkit**: Statistical models for patient outcome predictions and analysis of treatment effectiveness.

- ## Financial Analytics
  - **Objective**: Forecasting market trends and assessing investment risks.
  - **Toolkit**: Time series analysis for market trend forecasting and risk assessment models.

- ## Sports Analytics
  - **Objective**: Optimizing team strategies and player performance.
  - **Toolkit**: Performance data analysis using logistic regression and Bayesian analysis.


With our scene set across the analytics spectrum, let's zoom in on the essence of analysis. Which is the Statistics behind the scenes in order to translate the



# Beyond the Basics: Elevating Your Data Game

![banner2](https://github.com/NumberHumanoid/Stats-101/assets/149428916/f7f1740a-1829-45e8-9a6e-9ac493418774)


- ## The Lexicon of Analytics

  - Every field has its jargon, and analytics is no exception. From the basic "mean" and "median" to the more esoteric "kurtosis," expanding your vocabulary is key to not just understanding the data, but communicating your findings effectively.
  - ## Key Definitions for Data Analysis

- Understanding the basics of data types and statistical tests is crucial for effective data analysis. Here are simplified definitions:

  - **Continuous**: Data that can take any value within a range, such as weight or time.

  - **Ordinal**: Data with a clear order but no fixed spacing between points, like race finishing positions.

  - **Nominal**: Categorical data without any specific order, similar to types of pizza (pepperoni, vegetarian, meat lovers).

  - **Normality**: The assumption that data follows a bell curve distribution, where most values are near the center.

  - **Parametric Tests**: Statistical tests based on assumptions about the data's distribution, usually normality.

  - **Paired or Unpaired**:
    - **Paired**: Comparing two sets of related data (e.g., before and after a lesson).
    - **Unpaired**: Comparing two sets of unrelated data (e.g., test scores between different demographics).

  - **Groups for Test**:
    - **One Group**: Analyzing changes within the same group under different conditions.
    - **Two Groups**: Comparing differences between two separate groups.
    - **More Groups**: Comparing more than two groups against each other.

 - These foundational concepts pave the way for insightful and accurate data analysis.


- ## Understanding Hypothesis Testing

  - Peeling back the layers of data starts with hypothesis testing, the bedrock of making sense of the numbers. It's about asking the right questions and using statistical tests to uncover whether our assumptions hold water. Think of it as the detective work of analytics, where every clue (data point) brings us closer to solving the mystery.

- ## Selecting the Statistical Sword

  - Not all battles (data challenges) can be won with the same weapon (statistical test). Choosing the right test—be it t-tests for comparing means or chi-square tests for categorical data—is crucial. It's about matching your analytical arsenal to the question at hand, ensuring your insights are both accurate and actionable.
  
  - The selection between the statistical test depends on:
    - 1. What is the Question? Analyzing: (Difference or Relationship)
    - 2. What is the scale of the data? (Continuous, Ordinal or Nominal)
    - 3. What are some Assumptions for parametric tests? (Normality)
    - 4. What is the Experimental Design? (e.g. paired or unpaired design)
    - 5. What is Number of Groups? (One, Two or more groups) 

- ## Mastering Samples and Surveys

  - Data collection is an art form. Crafting surveys and designing samples that truly represent your population is foundational. This stage is all about gathering the golden nuggets of data without introducing bias, setting the stage for meaningful analysis.

- ## The Finer Points of Test Selection

  - Dive deeper into the art of test selection, navigating through the nuances of data types, distribution, and sample sizes. This lesson is your compass in the often complex landscape of statistical analysis, guiding you to the most effective tools for your analytical journey.

# Types of Statistical Tests
- ![Stat-sword](https://github.com/NumberHumanoid/Stats-101/assets/149428916/70bcee44-461b-4bed-bb06-1b3f98bc754e)
- ![stat-sword2](https://github.com/NumberHumanoid/Stats-101/assets/149428916/1f1cc571-27f2-4036-b3fd-95e51b8e81ec)

## Chi-Square & Z Tests: Unraveling Categorical Data

![banner-z](https://github.com/NumberHumanoid/Stats-101/assets/149428916/e2c2a717-9f4d-4050-a2dc-fdc56f054625)

- ## One-Proportion Z Test
  - #### Expectations and Outputs: The One-Proportion z Test evaluates whether the observed proportion of a categorical outcome (e.g., success vs. failure) differs from an expected proportion.
  - **Output to Look For:** The key output is the p-value. A p-value less than the chosen significance level (typically 0.05) suggests that the observed proportion significantly differs from the expected.
  - **Interpretation:** Alongside the p-value, you'll receive a test statistic (z-value) and a confidence interval for the proportion. The z-value indicates how many standard deviations the observed proportion is from the expected, while the confidence interval provides a range of plausible values for the true proportion.

  - #### (Ex:) Validating Hypotheses with a One-Proportion z Test
    - **Scenario**: Analyzing if the proportion of survey respondents favoring a new policy exceeds 50%.
    - **R Example**: `prop.test(x = 120, n = 200, p = 0.5, alternative = "greater")`
    - **Expected Outcome**: The p-value determines if the observed proportion (60%) significantly exceeds the hypothesized 50%. A p-value < 0.05 indicates significant support for the policy.

 
![chi](https://github.com/NumberHumanoid/Stats-101/assets/149428916/70adcec4-a81a-4236-b2a4-ba6d76dd1b95)

- ## Chi-Square Goodness of Fit Test
  - #### Expectations and Outputs: This test compares the observed frequencies of categories to expected frequencies to see if they deviate significantly.
  - **Output to Look For:** The chi-square statistic and the associated p-value. The larger the chi-square statistic, the more the observed data deviate from the expected distribution.
  - **Interpretation:** A significant p-value indicates that the observed frequencies across categories do not fit the expected distribution. The test doesn't tell you where the differences lie, only that at least one category frequency significantly differs.
 
  - #### (Ex:) Ensuring Your Data Fits the Expected Distribution
    - **Scenario**: Testing if feed type affects weight gain evenly across all types in the `chickwts` dataset.
    - **R Example**: `chisq.test(table(chickwts$feed))`
    - **Expected Outcome**: The chi-square statistic and p-value assess if observed frequencies match expected frequencies. A significant p-value suggests a distribution difference across feed types.


- ## Chi-Square Test of Independence
  - #### Expectations and Outputs: Used to determine if there’s a significant association between two categorical variables.
  - **Output to Look For:** Similar to the goodness of fit test, focus on the chi-square statistic and p-value.
  - **Interpretation:** A significant p-value suggests a significant association between the variables. The strength and direction of the association are not provided by this test but can be explored further with measures of association like Cramer’s V.
 
  - #### (Ex:) Exploring Relationships Between Categorical Variables
    - **Scenario**: Investigating if there's a relationship between the number of cylinders (`cyl`) and gears (`gear`) in cars.
    - **R Example**: `chisq.test(table(mtcars$cyl, mtcars$gear))`
    - **Expected Outcome**: A significant p-value indicates a significant association between cylinders and gears, suggesting certain gear types may be preferred for specific cylinder counts.




## T Tests: Comparing Means Across Groups
 
![T-test](https://github.com/NumberHumanoid/Stats-101/assets/149428916/37bdc4ed-162c-497a-8ae9-0cfe2f12e922)


- ## Paired-Sample t Test
  - #### Expectations and Outputs: Compares the means of two related groups to determine if there is a significant difference between them.
  - **Output to Look For:** The key outputs are the mean difference, t-value, degrees of freedom, and the p-value.
  - **Interpretation:** The mean difference tells you the average difference between the paired observations. A significant p-value indicates that this difference is not likely due to chance. The sign of the mean difference can also give direction to the change (increase or decrease).

  - #### (Ex:) Comparing Related Samples
    - **Scenario**: Measuring performance before and after a training program.
    - **R Example**: `t.test(sleep$extra[sleep$group == 1], sleep$extra[sleep$group == 2], paired = TRUE)`
    - **Expected Outcome**: The p-value reveals if the mean difference in sleep improvement is significant. A significant p-value implies the training program had a measurable effect on performance.


- ## Independent-Samples t Test
  - #### Expectations and Outputs: Assesses if there are significant differences between the means of two independent groups.
  - **Output to Look For:** Similar to the paired-sample t test, but with two sample means compared. Pay attention to the t-value, degrees of freedom, and p-value.
  - **Interpretation:** A significant p-value suggests a significant difference between group means. Confidence intervals for the mean difference can provide insight into the magnitude and direction of the difference.

  - #### (Ex:) Analyzing Differences Between Two Independent Groups
    - **Scenario**: Comparing mileage between 4-cylinder and 6-cylinder cars.
    - **R Example**: `t.test(mpg ~ cyl, data = mtcars, subset = cyl %in% c(4, 6))`
    - **Expected Outcome**: A significant p-value suggests a significant difference in mileage between the two car types, indicating efficiency varies with cylinder count.


## ANOVA & Tukey’s HSD: Exploring Variations Across Multiple Groups
 
![ANOVA](https://github.com/NumberHumanoid/Stats-101/assets/149428916/acaab21c-0c08-4367-aadd-63ba6d208b87)


- ## One-way ANOVA
  - #### Expectations and Outputs: Tests whether there are significant differences among the means of three or more independent groups.
  - **Output to Look For:** The F-statistic and its corresponding p-value. The F-statistic compares the variance between groups to the variance within groups.
  - **Interpretation:** A significant p-value indicates that at least one group mean significantly differs from the others. It doesn’t specify which groups are different, necessitating post-hoc tests like Tukey’s HSD for detailed comparisons.

  - #### (Ex:) Identifying Differences Among Group Means
    - **Scenario**: Testing if different treatments affect plant growth.
    - **R Example**: `anova_result <- aov(weight ~ group, data = PlantGrowth)`
    - **Expected Outcome**: ANOVA's F-statistic and p-value determine if growth differs significantly across treatments. A significant p-value warrants further investigation with Tukey's HSD.


- ## Tukey's HSD
  - #### Expectations and Outputs: A post-hoc comparison test used after ANOVA to identify specific group differences.
  - **Output to Look For:** The difference between group means, confidence intervals, and a p-value for each pair of groups compared.
  - **Interpretation:** Focus on pairs with a significant p-value to identify where the differences lie. The confidence intervals help understand the range of possible mean differences, providing a measure of effect size.

  - #### (Ex:) Pinpointing Specific Group Differences
    - **Following ANOVA**: To identify which groups differ.
    - **R Example**: `TukeyHSD(anova_result)`
    - **Expected Outcome**: Identifies specific pairs of treatments with significant differences in mean growth, helping refine agricultural practices.



## Correlation Analysis: Pearson and Spearman
 
![banner_corr](https://github.com/NumberHumanoid/Stats-101/assets/149428916/56bb892d-1ee4-42df-826a-d56f0e7ef0a7)


- ## Pearson Correlation
  - #### Expectations and Outputs: Measures the linear relationship between two continuous variables.
  - **Output to Look For:** The Pearson correlation coefficient (r) ranges from -1 to 1, and the associated p-value.
  - **Interpretation:** The coefficient indicates the strength and direction of the linear relationship. A significant p-value suggests the
 
    - #### (Ex:) Measuring Linear Relationships
      - **Scenario**: Exploring the relationship between blood pressure and body mass index (BMI).
      - **Expected Outcome**: The Pearson correlation coefficient (r) indicates the strength and direction of the linear relationship, with a significant p-value confirming the correlation's reliability.



# References

- Matthew Russell (Statistics in Natural Resources) https://stats4nr.com/
- Nancy Seby (GeeksforGeeks) https://www.geeksforgeeks.org/11-industries-that-benefits-the-most-from-data-science/
- James Chen (Investopedia) https://www.investopedia.com/contributors/101529/
- Andreas Tilevik (TileStats) https://www.youtube.com/watch?v=dYJLUvo0Q6g
