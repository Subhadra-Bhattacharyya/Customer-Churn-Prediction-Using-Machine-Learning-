# 📉 Customer Churn Prediction using Machine Learning

This project predicts whether a customer is likely to **churn (leave the service)** for a telecom company using supervised machine learning techniques. It includes end-to-end development — from data cleaning and feature engineering to model training, evaluation, and deployment.

---

## 🗂️ Dataset

- **Source**: Telco Customer Churn Dataset (IBM Sample)
- **Rows**: 7,043 customers
- **Target**: `Churn` (Yes / No)
- **Features**: Demographics, service usage, billing info, contract types

---

## 🧠 ML Models Used

| Model            | Accuracy (CV) |
|------------------|---------------|
| Decision Tree    | 78%           |
| XGBoost          | 83%           |
| ✅ Random Forest | **84%**       |

Random Forest was chosen for final deployment.

---

## 🔍 Project Workflow

1. **Data Cleaning**
   - Removed non-informative columns like `customerID`
   - Fixed blank values in `TotalCharges` column
   - Converted data types appropriately

2. **Exploratory Data Analysis (EDA)**
   - Visualized distributions of numerical and categorical features
   - Detected churn trends in contract types and payment methods

3. **Preprocessing**
   - Label-encoded all categorical columns using `LabelEncoder`
   - Handled class imbalance using **SMOTE**

4. **Model Training**
   - Trained Decision Tree, Random Forest, and XGBoost
   - Evaluated using 5-fold cross-validation and test set performance

5. **Model Deployment**
   - Saved model as `customer_churn_model.pkl`
   - Saved encoders as `encoders.pkl`
   - Built a **user-input based prediction system**

---

## 📊 Sample User Input for Prediction

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
📈 Results (Test Set)
Metric	Score
Accuracy	77.8%
Precision	58%
Recall	59%
F1-Score	58%

💾 Project Files
File	Description
Churn_Prediction.ipynb	Main Colab notebook
customer_churn_model.pkl	Trained Random Forest model
encoders.pkl	Saved label encoders
Telco-Customer-Churn.csv	Dataset used for training

🛠 Technologies Used
Python (Pandas, NumPy)

Scikit-learn, XGBoost

imbalanced-learn (SMOTE)

Seaborn & Matplotlib (EDA)

Pickle (model serialization)

Google Colab

🚀 Future Enhancements
Hyperparameter tuning with GridSearchCV or Optuna

Model explainability using SHAP/LIME

Deploy as a web app using Streamlit or Flask

Integrate into real-time churn monitoring system

👩‍💻 Author
Subhadra Bhattacharyya
Aspiring Data Scientist | Machine Learning Enthusiast
contact: subhadrabhattacharyya7@gmail.com
