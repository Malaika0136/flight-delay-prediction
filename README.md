# ✈ Weather and Flight Delay Prediction

This project analyzes and predicts flight delays using machine learning techniques applied to both weather and flight schedule data. All code and analysis are contained within a single Jupyter Notebook.

---

##  Project Overview

The notebook implements three machine learning models using the **Random Forest** algorithm:

- **Binary Classification** — Predict whether a flight will be delayed.
- **Multiclass Classification** — Categorize the severity of delay (No, Short, Moderate, Long).
- **Regression** — Predict the exact delay time in minutes.

---

##  Dataset Preprocessing

- **Cleaning**: Removed irrelevant columns and handled missing values.
- **Encoding**: Categorical variables (e.g., IATA codes, status) encoded using Label Encoding.
- **Scaling**:
  - `Normalize()` for binary classification.
  - `StandardScaler` for multiclass and regression models.

---

## 🔍 Model Highlights

###  Binary Classification
- **Target**: `Delay_Label` (Delayed vs. On-Time)
- **Model**: Random Forest Classifier
- **Validation Accuracy**: 90.3%
- **Evaluation**: Confusion Matrix, Precision-Recall Curve
- **Tuning**: Optimized `n_estimators`, `max_depth`, `min_samples_split`

###  Multiclass Classification
- **Target**: Delay severity (4 categories via `pd.cut`)
- **Model**: Random Forest Classifier
- **Accuracy**: 87.3%
- **Evaluation**: Classification Report, Confusion Matrix
- **Tuning**: Cross-validation + hyperparameter tuning

###  Regression
- **Target**: Exact delay time (continuous)
- **Model**: Random Forest Regressor
- **MAE**: 1.1 minutes  
- **RMSE**: 2.2 minutes
- **Evaluation**: Cross-validation, feature importance visualization

---

##  Key Insights

- **Weather Conditions** (temperature, wind speed, humidity) significantly impact delays.
- **Flight Schedules** (e.g., hour of departure) correlate with delay likelihood.
- **Random Forest Models** performed consistently well across all tasks.

---

##  How to Use

1. Clone the repository:
   ```bash
   git clone https://github.com/Malaika0136/flight-delay-prediction.git
   cd flight-delay-prediction
