# Predicting heart disease using machine learning
## 1. Problem Definition

In a statement, 
> Given clinical parameters about a patient, can we predict whether or not they have heart disease?

## 2. Data

The original dat acame from the Clevland data from the UCI Machine Learning Repository. https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data

There is also a version of it available on Kaggle. https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data

## 3. Evaluation

> If we can reach 95% accuracy at predicting wether or not a patient has heart disease during the proof of concept, we'll pursue the project.

## 4. Features
This is where you'll get different information about each of the features in your data.

Heart Disease Dataset Data Dictionary
| Column | Description | Values / Key |
| :--- | :--- | :--- |
| **age** | Age of patient | Years |
| **sex** | Gender | `1` = Male, `0` = Female |
| **cp** | Chest pain type | `0` = Typical Angina<br>`1` = Atypical Angina<br>`2` = Non-anginal Pain<br>`3` = Asymptomatic |
| **trestbps** | Resting blood pressure | mm Hg (Concern: >130–140) |
| **chol** | Serum cholesterol | mg/dL (Concern: >200) |
| **fbs** | Fasting blood sugar > 120 mg/dL | `1` = True, `0` = False (Diabetes: >126) |
| **restecg** | Resting ECG results | `0` = Normal<br>`1` = ST-T wave abnormality<br>`2` = Left ventricular hypertrophy |
| **thalach** | Max heart rate achieved | Beats per minute |
| **exang** | Exercise-induced angina | `1` = Yes, `0` = No |
| **oldpeak** | ST depression from exercise | Numeric stress level |
| **slope** | Peak exercise ST segment slope | `0` = Upsloping<br>`1` = Flat<br>`2` = Downsloping |
| **ca** | Major vessels colored by fluoroscopy | `0` to `3` |
| **thal** | Thallium stress result | `1` or `3` = Normal<br>`6` = Fixed defect<br>`7` = Reversible defect |
| **target** | Heart disease diagnosis | `1` = Yes, `0` = No |