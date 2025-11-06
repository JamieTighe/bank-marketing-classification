# Bank Marketing – Imbalanced Classification

This notebook uses the UCI Bank Marketing dataset to predict whether a customer will subscribe to a term deposit (`y`).

### Goal
Because the data is highly imbalanced (most customers say “no”), the main objective is to find a model that performs well on the **positive** class, not just overall accuracy.

### What I did
- Loaded and cleaned the data
- One-hot encoded categorical features with `pandas.get_dummies`
- Split into train/test
- Trained baseline models:
  - Logistic Regression
  - Random Forest
- Handled imbalance with:
  - SMOTE
  - RandomOverSampler
  - RandomUnderSampler / NearMiss (for comparison)
- Compared models using **F1 score**

### Best result
Logistic Regression trained on oversampled data (RandomOverSampler) → **F1 ≈ 0.44**.

### Files
- `bank_marketing_classification.ipynb` – main notebook
