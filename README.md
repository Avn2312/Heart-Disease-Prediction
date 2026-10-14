# Heart Disease Prediction using Machine Learning

A machine learning project that predicts the presence of heart disease in patients based on clinical features using the Cleveland UCI Heart Disease dataset.

---

## 📌 Project Overview
- **Objective:** Predict whether a patient has heart disease (`target = 1`) or not (`target = 0`) given medical attributes.
- **Problem Type:** Supervised Binary Classification.
- **Dataset:** 303 patient records with 13 clinical features.
- **Best Model:** **Logistic Regression** (Cross-validated Accuracy: **~84.8%**, AUC: **~0.93**).

---

## 📊 Dataset Features

| Feature | Description | Values / Normal Range |
| :--- | :--- | :--- |
| `age` | Age in years | 29–77 |
| `sex` | Gender | 1 = Male; 0 = Female |
| `cp` | Chest pain type | 0: Typical angina, 1: Atypical, 2: Non-anginal, 3: Asymptomatic |
| `trestbps` | Resting blood pressure | mm Hg (concerns if > 130–140) |
| `chol` | Serum cholesterol | mg/dL (> 200 is elevated) |
| `fbs` | Fasting blood sugar | > 120 mg/dl (1 = true; 0 = false) |
| `restecg` | Resting ECG results | 0: Normal, 1: ST-T wave abnormality, 2: LV hypertrophy |
| `thalach` | Max heart rate achieved | Exercise test heart rate |
| `exang` | Exercise-induced angina | 1 = Yes; 0 = No |
| `oldpeak` | ST depression | Induced by exercise relative to rest |
| `slope` | Slope of peak exercise ST | 0: Upsloping, 1: Flat, 2: Downsloping |
| `ca` | Number of major vessels | 0–3 colored by fluoroscopy |
| `thal` | Thallium stress result | 1, 3: Normal; 6: Fixed defect; 7: Reversible defect |
| `target` | Diagnosis | 1 = Heart Disease, 0 = No Disease |

---

## 🛠️ Models & Workflow
1. **Exploratory Data Analysis (EDA):** Feature distribution, correlation matrix heatmap, cross-tabulations.
2. **Model Comparison:** Evaluated baseline performance across:
   - Logistic Regression
   - K-Nearest Neighbors (KNN)
   - Random Forest Classifier
3. **Hyperparameter Tuning:**
   - Manual tuning for KNN (`n_neighbors`).
   - `RandomizedSearchCV` for Logistic Regression and Random Forest.
   - `GridSearchCV` fine-tuning for Logistic Regression (`C=0.2043`, `solver='liblinear'`).
4. **Evaluation Metrics (5-Fold Cross-Validation):**
   - **Accuracy:** 84.8%
   - **Precision:** 82.2%
   - **Recall:** 88.8%
   - **F1 Score:** 85.8%
   - **ROC-AUC:** ~0.93

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/Heart-Disease-Prediction.git
cd Heart-Disease-Prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook heart-disease-classification.ipynb
```
