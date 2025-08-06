# 🏠 Real Estate Lead Conversion Analysis – Moreno Valley, CA Metro Area

This project simulates and analyzes user behavior on a real estate platform to predict which users are most likely to contact an agent after viewing property listings. By modeling engagement patterns such as saving, sharing, and scheduling showings, we help prioritize follow-ups and support data-driven product decisions.

## 📍 Project Context
**Metro Area:** Moreno Valley, CA  
**Goal:** Predict agent contact likelihood based on user engagement actions and browsing patterns.  
**Data Source:** Simulated user-session dataset with multiple cookies grouped under unique user IDs.

---

## 🔍 Problem Statement
Real estate platforms often capture large volumes of anonymous session data. To increase lead conversion and improve resource allocation, it's important to identify high-intent users based on their engagement behavior.

We simulate and analyze user engagement metrics to:
- Predict which users are likely to contact an agent
- Recommend product or marketing strategies based on behavioral signals
- Compare interpretable and complex models for stakeholder decision-making

---

## 🧪 Modeling Approach
### Preprocessing
- Grouped cookies under user IDs to mimic cross-device behavior
- Engineered features: listings saved, shared, scheduled, session length, city viewed
- Balanced classes using SMOTE to address contact class imbalance

### Models Evaluated
- Logistic Regression
- Random Forest
- Gradient Boosting Classifier

| Model               | Recall | Precision | F1 Score |
|--------------------|--------|-----------|----------|
| Logistic Regression| 0.85   | 0.23      | 0.36     |
| Gradient Boosting  | 0.80   | 0.25      | 0.38     |
| Random Forest      | 0.49   | 0.39      | 0.43     |

---

## ✅ Recommendation

We recommend the **Logistic Regression** model due to its:
- **High recall (0.85)**: Effectively flags potential leads for follow-up.
- **Interpretability**: Business teams can easily understand the effect of key behaviors (e.g., saving listings) through odds ratios.
- **Similar F1 score** to more complex models, without sacrificing explainability.

---

## 📈 Key Insights

### Engagement Actions
- Users who **save listings** are nearly **3x more likely** to contact an agent.
- Sharing listings and scheduling showings also strongly increase conversion likelihood.
- **Product recommendation**: Prioritize features and nudges that encourage saving and sharing.

### Browsing Behavior
- Longer session lengths have a slight positive effect on contact rates.
- Viewing **more distinct listings** is **negatively associated** with contacting agents — suggesting a need to improve listing relevance.

### Location Signals
- Users viewing **Moreno Valley and Perris** listings show marginally higher contact rates.
- These geographic signals can inform local agent allocation or city-specific campaigns.

---

## 📌 Next Steps

- Implement UI features that encourage **saving and sharing**.
- Monitor and A/B test listing recommendation algorithms to optimize **session quality**.
- Leverage model outputs to segment users and trigger timely agent outreach or retargeting.
- Continue improving model precision by tuning thresholds or using cost-sensitive learning.

---

## 📁 File Structure

```bash
📦real-estate-contact-prediction/
├── data/
│   └── moval-zillow-data.csv
│   └── zillow-dataset-simulation.ipynb
├── notebooks/
│   └── moval-zillow-lead-conversion.ipynb
├── executive summary
│ 
├── README.md
```
