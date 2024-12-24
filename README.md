# Brain Stroke Prediction

This project predicts the likelihood of a brain stroke using machine learning models, with a focus on the Random Forest algorithm. Additionally, multiple classification models were evaluated for comparison. The project emphasizes robust data preprocessing and performance evaluation.

## Table of Contents

- [Introduction](#introduction)
- [Dataset Description](#dataset-description)
- [Data Preprocessing](#data-preprocessing)
- [Modeling](#modeling)
- [Results](#results)
- [Future Enhancements](#future-enhancements)

## Introduction

Stroke is a major cause of death and disability worldwide. This project predicts the risk of stroke based on patient data using machine learning techniques. The Random Forest model was selected for its robustness, and other classification models were also explored for comparative analysis.

## Dataset Description

The dataset contains patient details and stroke occurrences, obtained from a publicly available source such as [Kaggle](https://www.kaggle.com/). The key features include:

### Features

- **Age**: Patient's age
- **Gender**: Male, Female, or Other
- **Hypertension**: 0 if no hypertension, 1 if hypertension is present
- **Heart Disease**: 0 if no heart disease, 1 if heart disease is present
- **Ever Married**: Yes or No
- **Work Type**: Type of employment (e.g., Private, Self-employed, etc.)
- **Residence Type**: Urban or Rural
- **Average Glucose Level**: Average glucose level in the blood
- **BMI**: Body Mass Index
- **Smoking Status**: Smoking habits (e.g., Never smoked, Formerly smoked)
- **Stroke**: Target variable (1 if stroke occurred, 0 otherwise)

### Missing Values

- **BMI**: Contains missing values.
- **Other Features**: Fully populated.

## Data Preprocessing

Data preprocessing was performed to ensure high-quality inputs for the models. Key steps include:

### Handling Missing Values

- **BMI**: Imputed using median values grouped by `Age` and `Gender`.

### Encoding Categorical Variables

- **Gender, Ever Married, Work Type, Residence Type, Smoking Status**: Converted to numerical values using one-hot encoding.

### Scaling Numerical Features

- **Age, Average Glucose Level, BMI**: Scaled using Min-Max scaling for uniformity.

### Feature Engineering

- **Age Groups**: Binned `Age` into categories (child, young adult, adult, senior) for exploratory analysis.

### Data Splitting

- The dataset was split into training (80%) and testing (20%) sets using stratified sampling to maintain class distribution.

## Modeling

Multiple classification models were implemented and evaluated, including:

1. **Random Forest**: Primary model for prediction due to its high accuracy and feature importance insights.
2. **Logistic Regression**
3. **Support Vector Machine (SVM)**
4. **K-Nearest Neighbors (KNN)**
5. **Gradient Boosting (e.g., XGBoost, LightGBM)**
6. **Naive Bayes**

### Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC Score**

## Results

- **Best Model**: Random Forest achieved the highest performance with an accuracy of \~95% on the test set.
- **Feature Importance**: Key predictors included `Age`, `Average Glucose Level`, and `BMI`.
- Other models performed as follows:
  - Logistic Regression: \~80% accuracy
  - SVM: \~81% accuracy
  - Gradient Boosting: \~84% accuracy


## Future Enhancements

- Incorporating advanced feature selection techniques.
- Exploring ensemble methods for improved accuracy.
- Deploying the model using Flask or FastAPI for real-time predictions.
- Adding interpretability tools like SHAP for better model insights.



