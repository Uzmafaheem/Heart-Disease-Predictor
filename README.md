# 🩺 Heart Disease Prediction (Classification)

Predicting heart disease early can save lives. This project builds a Machine Learning classification model to determine whether a patient is likely to have heart disease based on clinical attributes. It serves as an excellent introduction to classification modeling, EDA, and model evaluation techniques.

## 📌 Project Objective

To develop a machine learning model that accurately predicts heart disease using patient medical data.
This project introduces key concepts in classification, including preprocessing, model training, and evaluation using standard ML metrics.


## 📥 Dataset Download

- The dataset is downloaded directly from Kaggle using the Kaggle Hub API:

       print("Downloading dataset...")
       path = kagglehub.dataset_download("redwankarimsony/heart-disease-data")

      file_path = f'{path}/heart_disease_uci.csv'
      df = pd.read_csv(file_path)

      print("Dataset downloaded and loaded successfully.")
      print(f"Data shape: {df.shape}")

## 🔍 Project Overview
1. Import Libraries & Load Dataset

- Load the heart disease dataset

- Explore basic structure & dimensions

- Identify missing values and data types

2. Exploratory Data Analysis (EDA)

- Visualize feature distributions

- Compare patterns between patients with & without heart disease

- Identify correlations and medically significant relationships

3. Data Preprocessing

- Encode categorical variables

- Scale numerical features

- Train-test split

4. Model Building

- We develop and compare two models:

  - Logistic Regression → baseline model

  - Random Forest Classifier → advanced ensemble model

  - Support Vector Machine (SVM)

5. Model Evaluation

- Metrics used:

- Accuracy

- Precision

- Recall

- F1-Score

- Confusion Matrix

6. Feature Importance

- Using Random Forest to identify critical medical attributes.

## 📊 Key Insights from EDA
✔ Dataset Balance

- The dataset is relatively balanced — slightly more patients with heart disease.
- This ensures accuracy remains a meaningful metric.

✔ Important Feature Patterns

- Max Heart Rate (thalach):
- Patients with heart disease tend to have lower max heart rate.

- Chest Pain Type (cp):

  - Types 1 and 2 → higher likelihood of heart disease

  - Type 0 → surprisingly lower risk

  - Type 3 (asymptomatic) → high risk

Sex:
- Higher proportion of females in this dataset show heart disease.

## 🤖 Model Performance Summary
| Model                   | Accuracy          | Precision (Weighted) | Recall (Weighted) | F1-Score (Weighted) | Notes                                                                        |
| ----------------------- | ----------------- | -------------------- | ----------------- | ------------------- | ---------------------------------------------------------------------------- |
| **Logistic Regression** | **0.58**          | 0.55                 | 0.58              | 0.56                | Strong for class 0, weaker for minority classes                              |
| **Random Forest**       | **0.56**          | 0.52                 | 0.56              | 0.54                | Good on class 0, moderate on class 1, struggles with minority classes        |
| **SVM**                 | **⭐ 0.59 (Best)** | **0.54**             | **0.59**          | **0.56**            | Best accuracy overall, best for class 1                                      |
| **KNN**                 | **0.58**          | 0.52                 | 0.58              | 0.55                | Similar to Logistic Regression but slightly lower minority-class performance |




## ⭐ Feature Importance (From Random Forest)

Most influential predictors:

- ca — number of major vessels colored by fluoroscopy

- thalach — maximum heart rate

- thal — thalassemia type

- cp — chest pain type

These findings match medical domain knowledge and the patterns observed in EDA.

## 🧠 Conclusion

This project demonstrates the entire workflow of a classification ML system —
from data loading, preprocessing, visualization, modeling, and evaluation, to interpreting model outputs.


- Random Forest is the most effective model for this dataset.

- Medical attributes like ca, thalach, thal, and cp play crucial roles.

- Proper preprocessing and evaluation are essential for trustworthy predictions.

- This project serves as a solid introduction to building end-to-end classification models in applied machine learning.

## 🚀 Future Improvements

- Hyperparameter tuning with GridSearchCV or Optuna

- Adding more ML models (XGBoost, LightGBM)

- Model explainability using SHAP

- Deploying as a web app with Streamlit or FastAPI

## 👤 Author
Faheemunnisa Syeda
Machine Learning & Applied Math Specialist
- 📧 syedafaheem7@gmail.com
- 🔗 GitHub: [https://github.com/syedafaheem7/]
- 🔗 linkedln: [https://www.linkedin.com/in/faheem-unnisa-s-6270888b/]
