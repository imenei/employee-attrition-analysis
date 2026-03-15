
# 👥 Employee Attrition Analysis

> A Machine Learning project to predict voluntary employee turnover, based on the IBM HR Analytics dataset.

---

## 📋 Description

This project analyzes the key factors influencing employee attrition and builds several classification models to predict whether an employee is likely to leave the company or not.

---

## 📁 Project Structure

```
📦 employee-attrition-analysis/
├── 📓 analyse_attirition_d_un_employe.ipynb   # Main notebook
├── 📄 HR.csv                                   # IBM HR Analytics dataset
└── 📖 README.md
```

---

## 📊 Dataset

- **Source:** IBM HR Analytics Employee Attrition & Performance
- **Size:** 1,470 employees × 35 features
- **Target:** `Attrition` (Yes / No)

### Key Features

| Feature | Type | Description |
|---|---|---|
| `Age` | Numerical | Employee age |
| `Attrition` | Categorical | Left or stayed (target) |
| `BusinessTravel` | Categorical | Travel frequency |
| `Department` | Categorical | Department |
| `MonthlyIncome` | Numerical | Monthly salary |
| `OverTime` | Categorical | Works overtime or not |
| `YearsAtCompany` | Numerical | Years at the company |
| `JobSatisfaction` | Numerical | Job satisfaction score (1–4) |
| `WorkLifeBalance` | Numerical | Work-life balance score (1–4) |
| ... | ... | 35 features total |

---

## 🔧 Project Pipeline

### 1. 📥 Loading & Exploration
- Load `HR.csv` dataset
- Analyze data types (`int64`, `object`)
- Descriptive statistics (mean, std, min/max)
- Missing value detection

### 2. 📈 Visualization
- Histograms of numerical features
- Attrition distribution by department, job role, gender
- Feature correlations

### 3. 🔨 Data Preprocessing
- One-Hot Encoding of categorical variables
- Dropping redundant columns (`EmployeeCount`, `Over18`, `StandardHours`)
- Train/test split (80/20)
- Feature normalization

### 4. 🤖 Models Trained

| Model | Description |
|---|---|
| **Decision Tree** | `DecisionTreeClassifier` |
| **SVM** | `SVC` (Support Vector Machine) |
| **Logistic Regression** | `LogisticRegression` |
| **KNN** | `KNeighborsClassifier` |

### 5. 📉 Evaluation
- Confusion matrix
- Classification report (Precision / Recall / F1-score)
- ROC curve & AUC score
- Decision boundary visualization (via PCA)

---

## 📏 Results

### Best Model — SVM / Logistic Regression

```
=== TEST ===
Accuracy : 86.73%

              precision    recall  f1-score   support

     0 (No)     0.87      1.00      0.93       247
    1 (Yes)     0.90      0.19      0.32        47

    accuracy                        0.87       294
   macro avg    0.88      0.59      0.62       294
weighted avg    0.87      0.87      0.83       294
```

### Prediction on a New Employee

```python
# Sample employee
Age=40, DailyRate=8000, YearsAtCompany=12, JobSatisfaction=3 ...

Decision Tree prediction : 0  → Will NOT leave ✅
SVM prediction           : 0  → Will NOT leave ✅
```

---

## 🚀 Getting Started

### Option 1 — Google Colab (recommended)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

```
1. Open Google Colab
2. Upload the .ipynb file
3. Upload HR.csv to /content/
4. Run all cells
```

### Option 2 — Run Locally

```bash
# Clone the repository
git clone https://github.com/your-username/employee-attrition-analysis.git
cd employee-attrition-analysis

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Launch Jupyter
jupyter notebook analyse_attirition_d_un_employe.ipynb
```

---

## 🛠️ Technologies

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-✓-150458?logo=pandas)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-✓-F7931E?logo=scikit-learn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-✓-11557c)
![Google Colab](https://img.shields.io/badge/Google%20Colab-✓-F9AB00?logo=googlecolab)

---

