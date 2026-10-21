# Feature Engineering

## What is Feature Engineering ? 

- Feature engineering is the process of creating new features.
- Because ML model don't understand the domain logic of our data.
- We do feature engineering to improve the accuracy of the model. 

## Techniques of Features Engineering

### 1. Mathematical combination: 

- Combining two features to get a new one

**Example:** 

|Area (sq ft)|Bedrooms|Price|
|---|---|---|
|1000|2|5000000|
|1500|3|7500000|
|2000|4|10000000|

|Area|Bedrooms|Price|**PricePerSqFt**|
|---|---|---|---|
|1000|2|5,000,000|5,000|
|1500|3|7,500,000|5,000|
|2000|4|10,000,000|5,000|
Here, `PricePerSqFt` is a new feature created by mathematical combination technique.

### 2. Target-based flags 

- We create a new feature based on the target variable

**For example:**
Suppose we are predicting ==whether a customer will buy a product:==

|Customer|Previous Purchases|Purchased|
|---|---|---|
|A|2|No|
|B|8|Yes|
|C|5|Yes|
We can create a flag like: 
```
FrequentBuyer = 1 if Previous Purchases >= 5
                0 otherwise
```

|Customer|Previous Purchases|Purchased|**FrequentBuyer**|
|---|---|---|---|
|A|2|No|0|
|B|8|Yes|1|
|C|5|Yes|1|

Here, we created a new feature called `FrequentBuyer` using Target-based method.

>[!caution] 
>In practice, be careful about creating features directly from the target itself, because that can cause data leakage. Usually we create the flag from information available before the target occurs.

### 3. Binning 

- Converting continuous data into range or groups

**For Example:**

|Person|Age|
|---|---|
|A|12|
|B|25|
|C|38|
|D|67|

Age can be divided into groups like:
```
0–17   → Child
18–30  → Young Adult
31–50  → Adult
51+    → Senior
```

|Person|Age|**AgeGroup**|
|---|---|---|
|A|12|Child|
|B|25|Young Adult|
|C|38|Adult|
|D|67|Senior|
Here, we created `AgeGroup` feature using binning. 

>[!note]
Instead of giving the model the exact value `38`, we can give it the category **Adult**.

### 4. Time-based features (like: dates)

- Convert dates into new features

**For Example:**

|Date|Sales|
|---|---|
|2026-01-05|120|
|2026-01-10|180|
|2026-02-15|250|

|Date|Sales|**Year**|**Month**|**Day**|**Day of Week**|
|---|---|---|---|---|---|
|2026-01-05|120|2026|1|5|Monday|
|2026-01-10|180|2026|1|10|Saturday|
|2026-02-15|250|2026|2|15|Sunday|

Here, we created `Year, Month and Day` feature using time-based features engineering.

#### Importance of Time-based feature: 

- The original `Date` alone may not tell the ML model much. But after extracting:

- **Year** → captures yearly trends
- **Month** → captures seasonal patterns
- **Day of week** → captures weekday/weekend behavior
- **Hour** → useful for hourly data
- **Weekend/weekday** → captures different customer behavior

**For example**, 
In a **cafe sales prediction** project:
```
Date: 2026-09-25 18:30
```
could become:
```
Year       = 2026
Month      = 9
Day        = 25
Hour       = 18
DayOfWeek  = Friday
Weekend    = 0
```

>[!important]
>The ML model can then learn patterns such as **sales being higher during evening hours or on weekends**.

## Summary

> [!tip] Summary
>
> | Category | Technique | What we do | Example |
> |---|---|---|---|
> | **Create** | **Mathematical Combination** | Combine features mathematically | `Price / Area` |
> | **Create** | **Target-Based Flags** | Create a `0/1` feature based on a relevant condition | `FrequentBuyer = 1 if purchases ≥ 5` |
> | **Transform** | **Binning** | Convert numerical values into ranges/groups | `Age 38 → Adult` |
> | **Extract** | **Time-Based Features** | Extract useful information from date/time | `9/25/2026 → Month, Day, Year` |


> [!tip]Summary
>
> ```text
>                FEATURE ENGINEERING
>                        │
>         ├──────────────┬──────────────┐
>         ↓              ↓              ↓
>      CREATE         TRANSFORM      EXTRACT
>         │              │              │
>         ↓              ↓              ↓
>    Mathematical     Binning       Time-Based
>    Combination                    Features
>         │
>         ↓
>       Flags
> ```

