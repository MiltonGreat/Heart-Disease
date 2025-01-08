# Heart Disease Classification

### Problem Statement

Heart disease remains a leading cause of death; early prediction can save lives.

### Solution Approach:

Data: Heart Disease dataset with features like age, cholesterol, and blood pressure.

Methods:

- Trained Logistic Regression, Random Forest, and SVM models.
- Conducted EDA to identify correlations (e.g., cholesterol levels with heart risk).
- Evaluated models using ROC-AUC and precision-recall metrics.
- Tools: Python (Scikit-learn, Matplotlib), Tableau.

### Results

Achieved 89% accuracy with Random Forest, highlighting high-risk patients.

### Challenges

Addressing class imbalance in the dataset.

### Future Directions

Incorporate time-series data for monitoring patient vitals.

### Key Skills

Predictive modeling, feature engineering, data visualization, Python.

### Summary and Recommendations

#### 1. Overview

This project is focused on predicting the likelihood of heart disease using machine learning models. The dataset used in this project includes various health metrics like blood pressure, cholesterol levels, and maximum heart rate, among others. The goal is to train multiple machine learning models to classify whether a patient is at risk of heart disease based on these features. The models are evaluated and compared to find the best performer, which is then saved for future predictions on new patient data.

The objective of this project is to use machine learning models to predict the presence of heart disease based on patient data. Key tasks include:

- Data cleaning and preprocessing.
- Training several models (Logistic Regression, Random Forest, and Support Vector Machine).
- Evaluating model performance using accuracy, precision, recall, and ROC-AUC.
- Hyperparameter tuning using GridSearchCV to optimize the Random Forest model.
- Saving the best-performing model for future use.

#### 2. Data

Dataset

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

#### 3. Approach

1. Data Preprocessing:
2. Model Training
- Logistic Regression: A linear model used for binary classification.
- Random Forest Classifier: An ensemble learning method that creates multiple decision trees and outputs the mode of the classes.
- Support Vector Machine (SVM): A robust classifier that finds the hyperplane that best separates the classes.
3. Model Evaluation:
4. Hyperparameter Tuning:
5. Feature Importance:
6. Model Prediction on New Data:

#### 4. Key Findings
      
All three models (Logistic Regression, Random Forest, and SVM) performed similarly in terms of accuracy (~86%) and AUC (>0.92), making them reliable predictors for heart disease. SVM and Logistic Regression slightly outperformed Random Forest in terms of ROC-AUC.

The Random Forest model revealed that features like MaxHR, Cholesterol, and Age had the most impact on predicting heart disease, providing valuable insights into the most important factors influencing heart disease risk.

Interpretation of Results: 

- The high accuracy and strong performance metrics across classes (e.g., normal and opacity) suggest that the model is well-suited for identifying both at-risk and non-at-risk patients.
- The use of Chest X-Ray images as inputs means the model is leveraging visual patterns, which are highly relevant for clinical diagnoses of conditions like pneumonia or other causes of mortality.

The final part of the code uses the best model to predict heart disease for a new patient. For example:

- Patient Info: 52 years old, RestingBP of 138, Cholesterol of 175, and MaxHR of 125.
- Prediction: The model predicts that the patient has heart disease.

#### 5.  Source

https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction
