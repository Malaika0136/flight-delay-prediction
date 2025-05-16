# flight-delay-prediction
📊 Weather and Flight Delay Prediction
This project analyzes and predicts flight delays using machine learning techniques applied to both weather and flight schedule data. All work — including data preprocessing, model training, evaluation, and visualization — is contained within a single Jupyter Notebook.

🚀 Project Overview
The notebook implements three models using the Random Forest algorithm:

Binary Classification — Predict whether a flight is delayed or not.

Multiclass Classification — Classify the delay severity (No, Short, Moderate, Long).

Regression — Predict the exact delay time in minutes.

📁 Dataset Preprocessing
Cleaning: Removed irrelevant columns and handled missing values.

Encoding: Converted categorical values (IATA codes, status) using Label Encoding.

Scaling:

Used Normalize() for binary classification.

Used StandardScaler for multiclass and regression models.

🔍 Model Highlights
✅ Binary Classification
Target: Delay_Label (Delayed vs. On-Time)

Accuracy: 90.3% (Validation)

Evaluation: Confusion Matrix, Precision-Recall Curve

Optimization: Tuned n_estimators, max_depth, min_samples_split

🔢 Multiclass Classification
Target: Delay severity (4 classes via pd.cut)

Accuracy: 87.3%

Evaluation: Classification Report, Confusion Matrix

Optimization: Cross-validation and parameter tuning

📈 Regression
Target: Continuous delay time

MAE / RMSE: 1.1 / 2.2 minutes

Optimization: Feature importance analysis, hyperparameter tuning

📊 Key Insights
Weather and Schedule strongly impact flight delays.

Random Forest models performed robustly across tasks.

Time of day (Scheduled Hour) is a useful predictive feature.
