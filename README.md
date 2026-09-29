# Employee Attrition Prediction using Machine Learning

A beginner-level machine learning project developed for **CSE422: Artificial Intelligence**.

This project explores employee attrition using an HR analytics dataset and applies supervised and unsupervised machine learning techniques to predict whether an employee is likely to stay or leave an organization.

## Authors

- Irfan Rahman
- Zarifah Morshed Nuren

**Course:** CSE422 - Artificial Intelligence  
**Section:** 4  
**Semester:** Summer 2026

---

## Project Overview

Employee turnover can create significant financial and operational challenges for organizations.

The objective of this project is to analyze employee-related factors and build machine learning models for predicting employee attrition.

The target variable is `Attrition`:

- `0` - Employee stayed
- `1` - Employee left

The project covers:

- Exploratory Data Analysis
- Data preprocessing
- Feature encoding and selection
- Feature scaling
- Supervised classification
- Neural networks
- Unsupervised clustering
- Model evaluation and comparison

---

## Dataset

The dataset contains:

- **1,677 records**
- **35 original features**
- **27 numerical features**
- **8 categorical features**

Example features include:

- Age
- Department
- JobRole
- MonthlyIncome
- JobSatisfaction
- OverTime
- YearsAtCompany
- WorkLifeBalance
- Attrition

The dataset was provided for the CSE422 lab project.

---

## Exploratory Data Analysis

Exploratory Data Analysis was performed to examine:

- Missing and duplicate values
- Attrition class distribution
- Feature distributions
- Skewness and outliers
- Numerical feature correlations
- Relationships between categorical features and attrition
- Multicollinearity among numerical features

The dataset contains a noticeable class imbalance, with significantly fewer employees in the `Left` class than in the `Stayed` class.

---

## Data Preprocessing

The preprocessing pipeline includes:

- Checking for null and duplicate values
- Removing constant and identifier features
- Binary encoding
- Ordinal encoding
- One-hot encoding
- Feature selection
- Stratified train-test splitting
- Feature scaling using `RobustScaler`

The scaler is fitted only on the training data to prevent information leakage.

---

## Machine Learning Models

The following models were implemented:

### Supervised Learning

- Neural Network
- Logistic Regression
- Gaussian Naive Bayes

### Unsupervised Learning

- K-Means Clustering

K-Means was trained without using the `Attrition` labels.

For evaluation, the cluster-to-class mapping was determined using the training data and then applied to the test data.

---

## Model Evaluation

The models were evaluated using:

- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1-Score
- ROC Curve
- AUC Score

### Results

| Model | Accuracy | Precision | Recall | F1-Score | AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.881 | 0.500 | 0.200 | 0.286 | 0.770 |
| Neural Network | 0.878 | 0.455 | 0.125 | 0.196 | 0.770 |
| Gaussian Naive Bayes | 0.682 | 0.198 | 0.550 | 0.291 | 0.700 |
| K-Means Clustering | 0.315 | 0.129 | 0.825 | 0.223 | 0.573 |

Logistic Regression achieved the highest overall accuracy and tied with the Neural Network for the highest AUC.

Gaussian Naive Bayes achieved substantially higher recall for the minority `Left` class, illustrating the trade-off between detecting more employees who leave and producing more false positives.

The results demonstrate why accuracy alone can be misleading for an imbalanced classification problem.

---

## Repository Structure

```text
employee-attrition-prediction/
│
├── data/
│   └── employee_attrition.csv
│
├── notebook/
│   └── employee_attrition_prediction.ipynb
│
├── report/
│   └── CSE422_employee_attrition_report.pdf
│
├── .gitignore
├── README.md
└── requirements.txt
```

---

## Project Files

- [Jupyter Notebook](notebook/employee_attrition_prediction.ipynb)
- [Project Report](report/CSE422_employee_attrition_report.pdf)
- [Dataset](data/employee_attrition.csv)

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras
- SciPy
- Jupyter Notebook / Google Colab

---

## How to Run

### 1. Clone the repository

```bash
git clone https://github.com/KryptOp76/employee-attrition-prediction.git
cd employee-attrition-prediction
```

### 2. Install the dependencies

```bash
pip install -r requirements.txt
```

### 3. Open the notebook

Open:

```text
notebook/employee_attrition_prediction.ipynb
```

using:

- Jupyter Notebook
- JupyterLab
- VS Code
- Google Colab

Then run the cells sequentially.

---

## Conclusion

This project demonstrates the complete workflow of a beginner-level machine learning classification problem, from exploratory data analysis and preprocessing to model training and evaluation.

The results also highlight an important consideration in imbalanced classification: the most appropriate model depends on the objective and evaluation metric rather than accuracy alone.

---

## Course Information

This project was completed as part of the lab project for **CSE422: Artificial Intelligence**.

The repository is intended for educational and academic purposes.
