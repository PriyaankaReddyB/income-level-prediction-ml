# Predicting Income Levels in the UCI Adult Dataset: A Machine Learning (ML) Perspective

## Project Overview

This project focuses on predicting income levels using the UCI Adult dataset (Census-Income dataset) to improve marketing and sales strategies for a retail company. By identifying high-income and low-income individuals, the company aims to create a data-driven segmentation strategy to target specific customer segments effectively.

---

## Problem Statement

To enhance marketing and sales strategies, the retail company seeks to create a segmentation strategy based on income categories. The goal is to improve targeting of customers, especially in the context of economic downturns and rising competition, while optimizing supply chain management through inventory planning.

---

## Potential Business Opportunities

1. **Better Business Decisions**: Making data-driven decisions on customer segmentation and targeting.
2. **Strategic Reevaluation**: Reassessing customer segments and strategies to overcome economic impacts.
3. **Supply Chain Optimization**: Improving inventory management to meet customer demand more effectively.

---

## Dataset Information

- **Dataset**: UCI Adult Dataset (Census-Income Dataset)  
  Sourced from the 1994 United States Census data.
- **Number of Records**: 48,842
- **Attributes**: 14 features (both categorical and continuous)

### Target Variable
- **Income**: The binary target variable indicating whether an individual earns more than $50,000 annually (equivalent to $104,000 annually, adjusted for inflation).

### Features
- **Age**: Age of the individual
- **Work-class**: Type of employment (Private, Local-gov, etc.)
- **Education**: Highest level of education completed
- **Education-Num**: Number of years of education
- **Marital Status**: Marital status (Married, Single, etc.)
- **Occupation**: Type of occupation
- **Relationship**: Relationship status (Husband, Wife, etc.)
- **Race**: Race (White, Asian-Pac-Islander, etc.)
- **Sex**: Gender of the individual
- **Capital Gain**: Capital gains reported
- **Capital Loss**: Capital losses reported
- **Hours Per Week**: Hours worked per week
- **Native Country**: Country of origin

---

## Data Preprocessing Steps

1. **Drop Unnecessary Columns**: Remove irrelevant columns such as `RELATIONSHIP`, `EDUCATION_NUM`, `FNLWGT`, `NATIVE_COUNTRY`, and `OCCUPATION`.
2. **Handle Missing Values**: Address missing data in `WORK_CLASS`.
3. **Encode Categorical Features**: Encode categorical variables like `WORKCLASS`, `EDUCATION`, `MARITAL_STATUS`, `RACE`, and `SEX`.
4. **Scale or Normalize Numerical Features**: Apply scaling to continuous features like `AGE`, `CAPITAL_GAIN`, `CAPITAL_LOSS`, and `HOURS_PER_WEEK`.

---

## Project Workflow

1. **Step 1**: Load the dataset.
2. **Step 2**: Data preprocessing, including handling missing values, encoding, and scaling.
3. **Step 3**: Split the dataset into training and test sets.
4. **Step 4**: Balance the data to handle class imbalance.
5. **Step 5**: Apply feature standardization to normalize data.
6. **Step 6**: Model selection and fitting using various machine learning algorithms.
7. **Step 7**: Perform hyperparameter tuning to optimize model performance.

---

## Machine Learning Models Used

- **Logistic Regression**
- **Random Forest**
- **Support Vector Machines (SVM)**
- **XGBoost**

### Model Performance Metrics

- **Accuracy**: Measure of the overall correctness of the model's predictions.
- **Precision**: Ability to accurately predict high-income individuals.
- **Recall**: Effectiveness of identifying all high-income individuals.
- **F1-Score**: A balance between precision and recall.
- **ROC-AUC**: Area under the ROC curve, representing the trade-off between true positive and false positive rates.

---

## Model Evaluation

| Model            | Accuracy (%) | Precision (%) | Recall (%) | F1-Score (%) | ROC-AUC (%) |
|------------------|--------------|---------------|------------|--------------|-------------|
| Logistic Regression | 82.1        | 60.36         | 82.79      | 69.24        | 90.02       |
| Random Forest     | 75.03        | 80.36         | 66.91      | 69.24        | 89.04       |
| XGBoost           | 79.30        | 54.57         | 84.46      | 66.30        | 90.66       |

- **True Positive (TP)**: High-income individuals correctly identified.
- **True Negative (TN)**: Low-income individuals correctly identified.
- **False Positive (FP)**: Low-income individuals incorrectly classified as high-income, leading to marketing inefficiencies.
- **False Negative (FN)**: High-income individuals incorrectly classified as low-income, missing potential business opportunities.

---

## Result

Among the models, **XGBoost** demonstrates the highest recall (84.46%), making it the most suitable model for the business scenario, as it effectively identifies the most high-income individuals. This model focuses on minimizing false negatives, which is crucial for ensuring that high-value customers are not overlooked.

By adopting the XGBoost model, the company can:

- Maximize recall, identifying the greatest number of high-income individuals.
- Ensure no high-income customers are missed, improving the effectiveness of customer targeting.
- Optimize marketing and sales strategies by focusing on the right customer segments.

The XGBoost model is recommended for the retail company's income-based segmentation strategy. Its higher recall ensures the identification of the maximum number of high-income individuals, leading to more targeted and effective marketing, inventory management, and overall business decisions.

---

## Conclusion

The Random Forest model is recommended for the retail company's income-based segmentation strategy. Its higher recall and balanced performance make it the best choice for identifying customer segments, leading to more effective marketing, inventory management, and overall business decisions.

---

## License

This project uses the UCI Adult Dataset, licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).
