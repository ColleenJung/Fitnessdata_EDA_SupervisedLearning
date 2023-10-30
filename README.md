# Fitnessdata_EDA_SupervisedLearning
#Decision trees vs Logistic regression 
## Problem Statement

The primary objective of this analysis was to understand and address the issue of churn in our fitness club. The problem statement can be summarized as follows:

- **Churn Rate:** The churn rate of 12% surpasses the 10% acquisition rate, which is having a negative impact on our total revenue. 

## Insights

During the exploratory data analysis (EDA) phase, several insights were uncovered:

1. **Lack of Correlations:** The correlation matrix revealed that numerical variables do not exhibit a strong correlation with churn. This suggests that we should focus on categorical variables to identify factors influencing churn.

2. **Churn Rate vs. Payment Type:** The analysis revealed that people who pay in cash and check are more likely to quit. This insight suggests that we may need to explore payment-related strategies to reduce churn.

3. **Usage vs. Default:** EDA highlighted that people who use the fitness center less frequently are more likely to quit. This indicates a need for strategies to stimulate usage among members.

## Logistic Regression (LR) vs. Decision Tree
![Sample Image](https://www.datasciencecentral.com/wp-content/uploads/2021/10/tempsnip2.jpg)
![Sample Image](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*KoAzQLM1zDi5s9yTR9V6hw.png)
![Sample Image](https://miro.medium.com/v2/resize:fit:1084/format:webp/1*U6twhNSe1I37feFfBaeXLw.png)
![Decision Tree](https://okanbulut.github.io/bigdata/images/decisiontree.png)


Here's a comparison between Logistic Regression (LR) and Decision Trees, highlighting the strengths and considerations for each method:

1. **Linearity:**
   - Decision trees support non-linearity, allowing them to capture complex, non-linear relationships between features.
   - Logistic Regression primarily models linear relationships, making it well-suited for problems with linear separability.

2. **Data Characteristics:**
   - When dealing with a large number of features and relatively fewer data points with low noise:
     - LR may outperform Decision Trees or Random Forests if the relationship is predominantly linear.
     - In general cases with more balanced data and a variety of relationships, Decision Trees tend to have better average accuracy.

3. **Categorical Independent Variables:**
   - Decision Trees are well-suited for handling categorical independent variables. They can naturally split on categories, eliminating the need for one-hot encoding.
   - LR requires categorical variables to be one-hot encoded, potentially leading to higher dimensionality.

4. **Handling Collinearity:**
   - Decision Trees can handle multicollinearity to some extent by selecting the most discriminative features at each split.
   - LR is sensitive to multicollinearity, and high multicollinearity can lead to unstable coefficient estimates.

The choice between LR and Decision Trees should be based on the specific characteristics of your data, the problem you are trying to solve, and your requirements for model interpretability and complexity. Consider the trade-offs and strengths of each method when deciding which one is best for your analysis.

## Decision Trees vs. Logistic Regression Result Comparison

- **Accuracy:** The logistic Regression model correctly predicted the default status (churn or not churn) for 88.09% while for the Decision Tree we got an accuracy level of 89.41% 
- **f-1 score:** Logistic Regression has low precision and recall for the "churn" class, resulting in a low F1-score(This indicates that the model is not effectively identifying cases of churn and is mainly predicting "not churn."). On the other hand, Decision Tree had class 0, it is 0.94, and for class 1, it is 0.55.
- **Interpretation:** Based on these results, the Decision Trees model has improved compared to the previous model based on logistic regression. It has better precision and recall for predicting "churn" (class 1) while maintaining high performance for predicting "not churn" (class 0). The F1-score for "churn" is also improved, indicating a better balance between precision and recall.
