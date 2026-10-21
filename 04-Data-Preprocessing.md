# Data Preprocessing

## What is Data Preprocessing? 

- Converting data into usable format 

- ML models cannot use **categorical data**. 
- We need to convert it into the **numerical format.**
  
## Steps of Data Preprocessing

### 1. Encoding Categorical Values 

- Converting categorical data into numbers because ML algorithms cannot use text data

#### a. Label Encoding

- Good for ordered (ordinal) data like: `low, medium, high` to `0, 1, 2` or binary data like: `male, female` to `0,1`, or `school, bachelor, master` to `0,1,2`

- Here `0,1` in gender doesn't represent order, it simply represent one of the two categories. 

#### b. One-Hot Encoding

- Good for data that doesn't have any natural order like: addresses `Kathmandu, Lalitput, Pokahara`, colors `red`, `blue`, `green`

- In this, the values are converted into a individual binary column to feed into the ML model.

**For eg:**

**In a House Price Prediction Model**

**Before One-Hot Encoding:**

| Area | Bedrooms | Location  | Price |
| ---- | -------- | --------- | ----- |
| 1200 | 3        | Kathmandu | 80L   |
| 1500 | 4        | Pokhara   | 90L   |
| 1000 | 2        | Lalitpur  | 70L   |

`Location` is categorical.

**After One-Hot Encoding:**

| Area | Bedrooms | Kathmandu | Pokhara | Lalitpur | Price |
| ---- | -------- | --------- | ------- | -------- | ----- |
| 1200 | 3        | 1         | 0       | 0        | 80L   |
| 1500 | 4        | 0         | 1       | 0        | 90L   |
| 1000 | 2        | 0         | 0       | 1        | 70L   |

Now all input features are numerical and can be given to the ML algorithm.

### 2. Feature Transformation

- It is used to handle skewed data like left-skewed right-skewed data. 
- It is changing form of the feature **without creating a new feature.** 

- We use `log`, `square root` for this.

### 3. Feature Scaling

- In this we, bring values to the same scale. 
- It is useful for distance based algorithm

#### a. Normalization (Min-Max Scaling)

- The value ranges between `0 and 1`

#### b. Standardization (Z-score)

- Transform data to have mean `0` and std `1`


