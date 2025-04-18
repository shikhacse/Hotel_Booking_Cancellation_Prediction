# 🏨 Hotel Booking Cancellation EDA & Prediction

This project analyzes hotel booking data to understand cancellation behavior and predict cancellations using various machine learning models.

---

# 📚 Table of Contents

- [1. Project Overview](#1-project-overview)
- [2. Exploratory Data Analysis (EDA)](#2-exploratory-data-analysis-eda)
- [3. Data Preprocessing](#3-data-preprocessing)
- [4. Model Building](#4-model-building)
- [5. Model Comparison](#5-model-comparison)
- [6. Conclusion](#6-conclusion)

---

# 1. Project Overview
- **Goal:** Predict whether a hotel booking will be canceled or not.
- **Type:** Binary Classification
- **Techniques:** 
  - Exploratory Data Analysis (EDA)
  - Data Cleaning
  - Feature Engineering
  - Multiple Machine Learning Models
  - Model Comparison

---

# 2. Exploratory Data Analysis (EDA)

### 📌 Where do the most guests come from?
- Most guests are from **Portugal (PRT)**, followed by the UK (GBR), France (FRA), and Spain (ESP).
- Created a **world map** to visualize guest distribution.

### 📌 How much do guests pay per night?
- Price (`adr`) varies depending on hotel type and room type.
- **City Hotel** and **Resort Hotel** show different pricing patterns.

### 📌 How does the price vary over the year?
- **Resort Hotel:** Peaks during **summer** (July, August).
- **City Hotel:** Higher rates in **Spring and Autumn**.

### 📌 Which are the busiest months?
- **City Hotel:** Peak guest counts in Spring and Autumn.
- **Resort Hotel:** Most bookings in Summer.

### 📌 How long do guests stay?
- Most guests stay between **1 to 3 nights**.

---

# 3. Data Preprocessing

### 📌 Handling Missing Values
- Filled missing values with 0.

### 📌 Data Cleaning
- Removed rows where `adults`, `children`, and `babies` were all zero.

### 📌 Feature Engineering
- Created a new feature `total_nights` by combining stay durations.
- Extracted `year`, `month`, and `day` from the reservation date.

### 📌 Encoding Categorical Variables
- Encoded features like `hotel`, `meal`, `market_segment`, `distribution_channel`, etc.

### 📌 Feature Selection
- Dropped low-importance columns such as `days_in_waiting_list`, `country`, and `reservation_status_date`.

### 📌 Normalization
- Applied **log transformation** on features with large variance (e.g., `lead_time`, `adr`).

---

# 4. Model Building

We trained and evaluated the following models:

| Model | Accuracy |
|:---|:---|
| Logistic Regression | 77.40% |
| K-Nearest Neighbors (KNN) | 88.54% |
| Decision Tree Classifier | 95.11% |
| Random Forest Classifier | 95.41% |
| AdaBoost Classifier | 95.08% |
| Gradient Boosting Classifier | 91.80% |
| XGBoost Classifier | 98.36% |
| CatBoost Classifier | **99.61%** |
| Extra Trees Classifier | 95.12% |
| LGBM Classifier | 96.11% |
| Voting Classifier | 98.36% |
| Artificial Neural Network (ANN) | 81.90% |

---

# 5. Model Comparison

- **CatBoost Classifier** achieved the highest accuracy: **99.61%**.
- **Voting Classifier** and **XGBoost** also performed extremely well (both **above 98%**).
- **Random Forest**, **Extra Trees**, and **LGBM** showed strong performances around **95%**.

**Visualization:**  
We plotted a bar chart comparing model performances using **Seaborn** (alternative to Plotly).

---

# 6. Conclusion

✅ Successfully performed full-cycle EDA, preprocessing, feature engineering, and machine learning modeling.

✅ Identified that cancellations are influenced by multiple factors like lead time, special requests, parking spaces, and repeat guests.

✅ Achieved a very high prediction accuracy using ensemble models like CatBoost, XGBoost, and Random Forest.

✅ Highlighted the importance of detailed data cleaning and feature selection in boosting model performance.

---

# 📂 Project Structure

| File | Description |
|:---|:---|
| `Hotel_Booking_Prediction.ipynb` | Complete notebook (EDA + Preprocessing + ML Models) |
| `hotel_bookings.csv` | Raw dataset |
| `README.md` | Project Overview (this file) |

---

# 📢 Notes
- Data preprocessing steps like log normalization significantly improved model training.
- CatBoost, XGBoost, and ensemble methods showed remarkable performance even without excessive hyperparameter tuning.

---
