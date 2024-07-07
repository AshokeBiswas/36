Q1. Difference between Linear Regression and Logistic Regression
Linear Regression:

Purpose: Predicts continuous numerical values.
Output: Predicted values can range from negative to positive infinity.
Example: Predicting house prices based on square footage and number of bedrooms.
Logistic Regression:

Purpose: Predicts binary outcomes (0 or 1, yes or no).
Output: Predicted values are probabilities between 0 and 1.
Example: Predicting whether a customer will churn (yes/no) based on their demographic data.
Scenario where Logistic Regression is More Appropriate:

When the dependent variable (target) is categorical or binary.
For classification tasks where the outcome is not numerical but a probability of belonging to a particular class.
Examples include predicting customer churn, classifying email spam, or diagnosing diseases.
Q2. Cost Function Used in Logistic Regression and Optimization
Cost Function (Log Loss or Binary Cross-Entropy):
𝐽
(
𝜃
)
=
−
1
𝑚
∑
𝑖
=
1
𝑚
[
𝑦
(
𝑖
)
log
⁡
(
ℎ
𝜃
(
𝑥
(
𝑖
)
)
)
+
(
1
−
𝑦
(
𝑖
)
)
log
⁡
(
1
−
ℎ
𝜃
(
𝑥
(
𝑖
)
)
)
]
J(θ)=− 
m
1
​
 ∑ 
i=1
m
​
 [y 
(i)
 log(h 
θ
​
 (x 
(i)
 ))+(1−y 
(i)
 )log(1−h 
θ
​
 (x 
(i)
 ))]

Penalizes incorrect predictions more heavily as the predicted probability diverges from the actual class label.
Goal: Minimize the cost function to optimize model parameters (
𝜃
θ).
Q3. Regularization in Logistic Regression
Purpose: Prevents overfitting by adding a penalty term to the cost function.

L2 Regularization (Ridge): Adds 
𝜆
∥
𝜃
∥
2
λ∥θ∥ 
2
  to the cost function.
L1 Regularization (Lasso): Adds 
𝜆
∥
𝜃
∥
λ∥θ∥ to the cost function.
Helps to shrink the coefficients towards zero, reducing model complexity.
Q4. ROC Curve and Its Use in Logistic Regression
ROC Curve (Receiver Operating Characteristic):

Plot: Graphical representation of the trade-off between true positive rate (Sensitivity) and false positive rate (1 - Specificity).
Evaluation: AUC (Area Under the Curve) summarizes the ROC curve's performance; higher AUC indicates better model performance.
Helps to visualize and compare different models' ability to discriminate between classes.
Q5. Techniques for Feature Selection in Logistic Regression
Common Techniques:

Stepwise Selection: Forward or backward selection based on model performance metrics (AIC, BIC).
Lasso Regression: Uses L1 regularization to shrink less important features' coefficients to zero.
Recursive Feature Elimination (RFE): Iteratively removes least important features based on model coefficients.
Principal Component Analysis (PCA): Reduces dimensionality while preserving variance.
Benefits: Improves model interpretability, reduces overfitting, and enhances model performance by focusing on relevant features.

Q6. Handling Imbalanced Datasets in Logistic Regression
Strategies:

Resampling Techniques: Oversampling minority class (SMOTE) or undersampling majority class.
Class Weight Adjustment: Assigning higher penalties to misclassifications of the minority class.
Ensemble Methods: Using techniques like bagging (Bootstrap Aggregating) or boosting (e.g., AdaBoost) to balance classes during training.
Goal: Prevents the model from being biased towards the majority class and improves prediction accuracy for the minority class.

Q7. Common Issues and Challenges in Logistic Regression
Multicollinearity:

Issue: High correlation among independent variables can lead to unstable estimates of coefficients.
Solution:
Remove one of the correlated variables.
Use regularization techniques like Ridge regression (L2) to shrink coefficients.
Principal Component Analysis (PCA) can reduce multicollinearity by transforming variables into uncorrelated principal components.
Other Challenges:

Non-linear Relationships: Logistic regression assumes linear relationships; transformations or non-linear models may be needed.
Outliers: Sensitivity to outliers; robust regression techniques or data preprocessing may be required.
Model Interpretability: Balancing between simplicity and accuracy; feature selection and regularization help maintain interpretability.
