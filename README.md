# 📉 Customer Churn Prediction - Machine Learning Project

This project predicts whether a customer will **churn (leave the service)** in a telecom company using historical usage and contract data. The goal is to help the company **retain customers** by identifying potential churners in advance.

---

## 📁 Dataset

- **Source**: Telco Customer Churn Dataset
- **Records**: 7043
- **Target Variable**: `Churn` (`Yes` or `No`)
- **Features**: Gender, SeniorCitizen, Tenure, MonthlyCharges, InternetService, Contract, PaymentMethod, etc.

---

## 🧠 Models Used

- Decision Tree Classifier
- Random Forest Classifier ✅ *(Best Performer)*
- XGBoost Classifier

---

## 🔍 Workflow Summary

1. **Data Cleaning**:
   - Removed irrelevant columns
   - Handled missing/blank values
   - Converted data types

2. **Exploratory Data Analysis (EDA)**:
   - Visualized numerical and categorical distributions
   - Examined correlations and outliers

3. **Data Preprocessing**:
   - Label encoded categorical features
   - Handled class imbalance using **SMOTE**

4. **Model Training**:
   - Used 5-fold cross-validation
   - Evaluated with Accuracy, Precision, Recall, F1-Score

5. **Model Selection**:
   - ✅ Random Forest achieved ~84% CV Accuracy

6. **Deployment Ready System**:
   - Saved model (`customer_churn_model.pkl`) and encoders
   - Built a **user-interactive prediction system** in Python

---

## 📊 Example Input for Prediction

```python
{
  'gender': 'Female',
  'SeniorCitizen': 0,
  'Partner': 'Yes',
  'Dependents': 'No',
  'tenure': 1,
  'PhoneService': 'No',
  'MultipleLines': 'No phone service',
  'InternetService': 'DSL',
  'OnlineSecurity': 'No',
  'OnlineBackup': 'Yes',
  'DeviceProtection': 'No',
  'TechSupport': 'No',
  'StreamingTV': 'No',
  'StreamingMovies': 'No',
  'Contract': 'Month-to-month',
  'PaperlessBilling': 'Yes',
  'PaymentMethod': 'Electronic check',
  'MonthlyCharges': 29.85,
  'TotalCharges': 29.85
}
