# 📝 moval-zillow-lead-conversion.ipynb

This notebook simulates and analyzes user behavior on a real estate platform (focused on the **Moreno Valley, CA** metro area) to predict whether a user will contact an agent after engaging with listings. It includes data generation, feature engineering, modeling, and insight generation.

---

## 📂 Notebook Overview

### 1. **Data Preprocessing & Feature Engineering**
- Groups cookies into unique user profiles
- Aggregates session-level metrics:
  - Average price viewed
  - Total saved/shared/scheduled counts
  - Session length
  - Unique cities browsed
- Encodes categorical data and scales numeric features

### 2. **Train-Test Split & SMOTE Balancing**
- Splits dataset into training and testing sets
- Applies **SMOTE** to balance the rare positive class (users who contacted an agent)

### 4. **Model Training & Evaluation**
- Compares performance of:
  - Logistic Regression
  - Random Forest
  - Gradient Boosting Classifier
- Metrics reported: Accuracy, Precision, Recall, F1 Score, AUC

### 5. **Insights & Recommendations**
- Identifies behaviors most correlated with contacting an agent
- Provides actionable business insights
