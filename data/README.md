# 🏠 Real Estate Lead Prediction — Data Folder

This folder contains the **synthetic dataset** used to model real estate lead prediction behavior, simulating user engagement on a home listing website in the **Moreno Valley, CA metro area**.

---

## 📁 Files

### `zillow-dataset-simulation.ipynb`
### `moval-zillow-data.csv`
Simulated dataset of ~26,000 browsing sessions over the past 180 days (6 months). Each row represents a single session from an anonymized user.

---

## 🧪 Data Generation Assumptions

This dataset was **entirely simulated** with the following domain-informed assumptions to reflect realistic patterns in the Moreno Valley housing market.

### 📍 Geographic Context
- **Cities Browsed:**
  - Moreno Valley: 300 listings
  - Perris: 285 listings
  - Riverside: 278 listings
  - Menifee: 150 listings

### 💲 Home Prices
- **Average Price Viewed:** $450,000
- **Standard Deviation:** $75,000
- **Price floor constraint:** No listings below 2 standard deviations ($300,000)

### 📐 Home Size
- **Average Square Footage Viewed:** 1,800 sq ft
- **Standard Deviation:** 300 sq ft
- **Sq Ft floor constraint:** No listings below 1,200 sq ft

### 👤 User Structure
- **500 total users** simulated
- **Max cookies per user:** 2 (e.g., phone + tablet)
- **Max sessions per cookie:** 5
- **Number of cities browsed per session:** Usually 1, occasionally 2–3

### 🕒 Session Activity
- **Session duration:** 10 to 30 minutes
- **Listings viewed per session:** Between 5 and 20

### 🔄 Engagement Actions
These user actions were simulated conditionally, depending on whether the user contacted an agent during the session:

| Action                | Probability if Contacted |
|-----------------------|--------------------------|
| Saved a listing       | 70%                      |
| Shared a listing      | 40%                      |
| Scheduled a showing   | 50%                      |

Sessions without agent contact were assigned significantly lower probabilities for these actions.

---

## 📌 Columns in `simulated_user_sessions.csv`

| Column               | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `session_id`         | Unique ID for the session                                                   |
| `cookie_id`          | Unique cookie/session identifier                                            |
| `user_id`            | User ID grouping multiple cookies together (e.g., phone and tablet)         |
| `city`               | City where listings were browsed                                            |
| `price_viewed`       | Average price of listings viewed during session                             |
| `sqft_viewed`        | Average square footage of listings viewed                                   |
| `num_listings_viewed`| Count of listings viewed during the session                                 |
| `duration_minutes`   | Duration of session                                                         |
| `saved`              | Whether user saved any listings                                             |
| `shared`             | Whether user shared any listings                                            |
| `scheduled`          | Whether user scheduled a showing                                            |
| `contacted`          | Whether user contacted an agent (target variable)                           |
| `timestamp`          | Date of session (within past 180 days)                                      |

---

## 📎 Notes
- This dataset is **synthetic**
- Designed to support a **classification modeling task** with a binary target: `contacted`.
- Engagement metrics and browsing behavior are structured to support **feature engineering and interpretability** for marketing or lead prioritization tasks.

