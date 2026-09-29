# Employee Attrition Prediction using Machine Learning

A beginner-level machine learning project developed for **CSE422: Artificial Intelligence**.

The project explores employee attrition using an HR analytics dataset and applies several supervised and unsupervised machine learning techniques to predict whether an employee is likely to stay or leave an organization.

## Authors

- Irfan Rahman
- Zarifah Morshed Nuren

**Course:** CSE422 - Artificial Intelligence  
**Semester:** Summer 2026

## Project Overview

Employee turnover can create significant financial and operational challenges for organizations. The objective of this project is to analyze employee-related factors and build machine learning models for predicting employee attrition.

The target variable is `Attrition`:

- `0` - Employee stayed
- `1` - Employee left

The project includes exploratory data analysis, preprocessing, feature selection, model training, and model evaluation.

## Dataset

The dataset contains:

- **1,677 records**
- **35 original features**
- **27 numerical features**
- **8 categorical features**

Some of the features include:

- Age
- Department
- Job Role
- Monthly Income
- Job Satisfaction
- OverTime
- Years at Company
- Work-Life Balance
- Attrition

## Project Workflow

### 1. Exploratory Data Analysis

The dataset was analyzed to investigate:

- Missing and duplicate values
- Class distribution
- Feature distributions and outliers
- Correlations with employee attrition
- Relationships between categorical features and attrition
- Multicollinearity between numerical features

### 2. Data Preprocessing

The preprocessing pipeline includes:

- Removing constant and identifier features
- Encoding categorical variables
- One-hot encoding nominal features
- Feature selection
- Stratified train-test splitting
- Robust feature scaling

### 3. Machine Learning Models

The following models were implemented:

- Neural Network
- Logistic Regression
- Gaussian Naive Bayes
- K-Means Clustering

K-Means was used as an unsupervised learning approach, while the other models were trained for supervised binary classification.

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

Logistic Regression achieved the highest overall accuracy and tied with the Neural Network for the highest AUC. However, Gaussian Naive Bayes achieved substantially higher recall for employees who actually left.

The results also demonstrate why accuracy alone can be misleading for an imbalanced classification problem.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- TensorFlow / Keras
- SciPy
- Google Colab

## Repository Structure

```text
.
├── data/
│   └── employee_attrition.csv
├── notebook/
│   └── employee_attrition_prediction.ipynb
├── report/
│   └── CSE422_employee_attrition_report.pdf
├── README.md
└── requirements.txt
