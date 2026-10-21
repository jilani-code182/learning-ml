## What is Feature Selection ?

- Selecting the useful feature and removing the rest
#### Importance
- Reduce noise and <span style="color:red">overfitting</span>
- Speed up training process
- Improve accuracy
- Makes model interpretation easier (need to takes less input from the user)

## Techniques for Feature Selection

### 1. Filter Method (pure statistics)

- **Correlation Matrix:** Remove highly correlated features
- **Chi-square test**: Categorical vs Categorical 
- **ANOVA F-test**: Numerical vs Categorical 

### 2. Embedded Method (selection built into model)

- **Lasso Regression**: Shrinks coefficient to 0
- **Tree-based models (Random Forest, XGBoost)**: Features importance scores 

