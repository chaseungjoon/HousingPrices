# Housing Prices

---

---

https://www.kaggle.com/competitions/home-data-for-ml-course

# Overview

Given 79 explanatory variables describing  every aspect of residential homes, predict the final price of each home. 

---

# Data

- train.csv - training set
- test.csv - test set
- data_description.txt - full description of each column
- sample_submission.csv - benchmark submission from linear regression

## Data Dictionary

Classify the variables into **tiers** based on **significance**

### Tier 1 (Most important)

- LotArea
- Street

### Tier 2 (Moderately important)

- MSSubClass
- MSZoning
- LotFrontage

### Tier 3 (Least important)

- Alley

## Submission Format

```cpp
Id, SalePrice
1461, 169000.1
1462, 187724.1233
1463, 175221
etc.
```

---

# Model

## All variables-model

Train a model using all variables → use tree-based models

## Tier-based variables-model

Train a model using selected variables → split into tiers regarding their significance

1. LR
2. Ridge
3. LGBM

---

# Results

| Submissions | Score | Submission Percentage (Top) |
| --- | --- | --- |
| All Features - Tree | 16516.02754 | 28.63% |
| TierSystem - LR | 16468.94362 | 26.93% |
| TierSystem - Ridge | 17625.58894 | 44.22% |
| TierSystem - LightGBM | 16183.21670 | 13.6% |