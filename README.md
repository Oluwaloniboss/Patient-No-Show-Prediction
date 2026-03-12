# 🏥 Patient No-Show Prediction

## 📋 Project Overview

This project analyzes over 110,000 medical appointments to predict patient no-shows using machine learning. The goal is to help healthcare providers identify high-risk patients and implement targeted interventions to reduce missed appointments, recover lost revenue, and improve healthcare access.

**Key Questions:**
- What factors contribute to patient no-shows?
- Can we predict which patients are likely to miss appointments?
- What interventions can reduce no-show rates?

## 📊 Dataset

- **Source:** [Medical Appointment No Shows](https://www.kaggle.com/datasets/joniarroba/noshowappointments) (Kaggle)
- **Records:** 110,527 appointments
- **Features:** 14 columns including patient demographics, health conditions, and appointment details
- **Target:** No-show (Yes/No)

## 🔍 Key Findings

| Insight | Finding |
|---------|---------|
| **Wait Time** | Patients waiting 30+ days have 35% no-show rate (vs 15% for same-day) |
| **Age** | Younger patients (18-35) miss appointments most frequently |
| **Welfare** | Scholarship patients have 23.4% no-show rate (vs 19.9%) |
| **SMS** | Counterintuitively, SMS reminders associated with higher no-shows (needs investigation) |
| **Chronic Conditions** | Patients with hypertension/diabetes show better attendance |

## 🛠️ Technical Approach

### Data Preprocessing
- Cleaned column names and handled missing values
- Converted date columns and engineered `WaitDays` feature
- Encoded categorical variables
- Standardized numerical features

### Models Tested
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)
- Decision Tree
- Random Forest

### Tools Used
- **Python** (Pandas, NumPy)
- **Visualization** (Matplotlib, Seaborn)
- **Machine Learning** (Scikit-learn)
- **Model Serialization** (Joblib)

## 📈 Results

| Model | Accuracy | Notes |
|-------|----------|-------|
| Logistic Regression | 79.58% | Baseline performance |

*Note: Class imbalance (20% no-show) affects minority class prediction. Future work will address this with SMOTE.*

## 💡 Recommendations

1. **Reduce wait times** – Schedule within 7 days when possible
2. **Enhance reminders** – Multi-channel, 48h + 24h before appointment
3. **Target high-risk groups** – Welfare patients, younger adults
4. **Predictive risk scoring** – Flag patients with >30% probability
5. **Operational improvements** – Saturday hours, mobile booking

## 🚀 Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
