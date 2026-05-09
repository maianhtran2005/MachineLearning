# Analysis and Prediction of Alzheimer's Disease Risk

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-Machine%20Learning-yellowgreen)
![XGBoost](https://img.shields.io/badge/XGBoost-Classification-red)

## 1. About The Project
Alzheimer's disease is a progressive neurodegenerative disorder that severely affects memory and cognitive functions. Early detection of the disease risk plays a crucial role in timely medical intervention and treatment.

This project analyzes a multi-dimensional medical dataset and applies Machine Learning algorithms to solve two main problems:
1. **Exploration and Clustering (Unsupervised Learning):** Discovering patient groups with similar underlying characteristic structures hidden within the data.
2. **Prediction and Classification (Supervised Learning):** Building models capable of classifying and predicting the risk of Alzheimer's disease based on medical records, lifestyle, and clinical indicators.

## 2. Dataset Description
The dataset used is `alzheimers_disease_data.csv`, consisting of **2,149 observations (patients)** and **35 attributes**. During preprocessing, identification columns (`PatientID`, `DoctorInCharge`) were removed. The main variable groups include:
* **Demographics & Lifestyle:** Age, Gender, Ethnicity, Education Level, BMI, Smoking, Alcohol Consumption, Physical Activity, etc.
* **Medical History & Clinical Indicators:** Family History, Cardiovascular Disease, Diabetes, Blood Pressure, Cholesterol (Total, LDL, HDL, Triglycerides), etc.
* **Cognitive/Functional Assessments:** MMSE, Functional Assessment, Behavioral Problems, ADL, etc.
* **Clinical Symptoms:** Confusion, Disorientation, Personality Changes, Forgetfulness, etc.
* **Target Variable:** `Diagnosis` (0: Negative/No Disease, 1: Positive/Has Disease).

## 3. Tech Stack & Methodology
* **Language & Libraries:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost.
* **Data Preprocessing:** Handling missing values, Scaling (`MinMaxScaler`, `StandardScaler`, `RobustScaler`).
* **Unsupervised Learning (Clustering):** * Dimensionality Reduction: PCA, t-SNE.
  * Algorithms: K-Means.
  * Evaluation: Silhouette score, Davies-Bouldin score, Calinski-Harabasz score.
* **Supervised Learning (Classification):**
  * Algorithms: Logistic Regression, Decision Tree, Random Forest, KNN, SVC, XGBoost.
  * Optimization: Hyperparameter tuning using `GridSearchCV`.
  * Evaluation: Confusion Matrix, Classification Report (Accuracy, Precision, Recall, F1-Score).
