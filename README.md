# Heart Disease Classification: Predicting Risk to Save Lives

## Overview

Heart disease is one of the leading causes of mortality worldwide. Early identification of at-risk individuals enables timely interventions, potentially saving lives and reducing healthcare costs. This project leverages machine learning models to predict heart disease based on patient health metrics. The Random Forest model achieved 89% accuracy, providing a robust tool to classify high-risk patients and guide preventive care strategies.

### Problem Statement

Heart disease accounts for a significant portion of global deaths, often due to late diagnosis. Accurate and early prediction of heart disease can improve clinical outcomes by enabling targeted preventive measures. This project aims to develop a machine learning-based solution to identify patients at risk of heart disease using readily available health indicators.

#### Dataset

The dataset used in this project contains patient data, including the following key features:

- Age: Patient's age.
- RestingBP: Resting blood pressure (mm Hg).
- Cholesterol: Serum cholesterol (mg/dL).
- FastingBS: Fasting blood sugar (1 if >120 mg/dL, else 0).
- MaxHR: Maximum heart rate achieved.
- Oldpeak: ST depression induced by exercise relative to rest.
- ChestPainType: Types of chest pain (ATA, NAP, TA).
- RestingECG: Resting electrocardiogram results (Normal, ST).
- ExerciseAngina: Whether the patient experiences exercise-induced angina (Yes/No).
- ST_Slope: Slope of the peak exercise ST segment (Flat, Up).

The target variable is HeartDisease, which indicates whether or not a patient has heart disease (1 for heart disease, 0 otherwise).

### Solution Approach:

1. Data Preprocessing
- Data Cleaning: Handled missing values and outliers.
- Feature Engineering: Encoded categorical variables (e.g., ChestPainType, RestingECG).
- Normalization: Scaled numeric features to improve model performance.

2. Exploratory Data Analysis (EDA)
- Analyzed the relationships between features like cholesterol, age, and exercise-induced angina with heart disease risk.
- Identified MaxHR and cholesterol levels as key indicators of heart disease.

3. Model Development
- Algorithms Tested: Logistic Regression, Random Forest, and Support Vector Machine (SVM).
- Feature Importance: Assessed key predictors using Random Forest.
- Hyperparameter Tuning: Optimized Random Forest using GridSearchCV.

4. Evaluation Metrics
- Accuracy: Assessed overall prediction success.
- ROC-AUC: Measured the model’s ability to distinguish between classes.
- Precision and Recall: Evaluated the model's reliability for identifying at-risk patients.

### Key Findings:

Model Comparison:
- All models (Logistic Regression, Random Forest, SVM) performed well, with ROC-AUC exceeding 0.92.
- Logistic Regression and SVM slightly outperformed Random Forest in ROC-AUC, indicating robustness across methods.

Patient Insights:
- High cholesterol levels and low MaxHR were strongly associated with heart disease risk.
- Male patients with high blood pressure were at elevated risk.

Example Prediction:
- Patient Info: 52 years old, RestingBP of 138, Cholesterol of 175, and MaxHR of 125.
- Prediction: The model classified this patient as high-risk for heart disease.

### Challenges

- Class Imbalance: Addressed using oversampling techniques to ensure balanced predictions.
- Feature Importance: Carefully selected and tuned features to avoid overfitting.

### Future Directions

1. Time-Series Analysis: Incorporate longitudinal patient data for dynamic monitoring of vitals and risk trends.

2. Model Deployment: Develop a web-based interface or API for real-time risk prediction.

3. Explainability: Use SHAP or LIME to make predictions interpretable for clinical use.

4. Broader Analysis: Extend the study to explore socio-economic and lifestyle factors.

# Source

https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction

