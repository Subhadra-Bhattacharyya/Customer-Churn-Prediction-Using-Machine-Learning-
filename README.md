
markdown
Copy
Edit
# 📉 Customer Churn Prediction using Machine Learning

This project predicts whether a customer is likely to **churn (leave the service)** for a telecom company using supervised machine learning techniques. It includes end-to-end development — from data cleaning and feature engineering to model training, evaluation, and deployment.

---

## 🗂️ Dataset

- **Source**: Telco Customer Churn Dataset (IBM Sample)
- **Records**: 7,043 customers
- **Target**: `Churn` (Yes / No)
- **Features**: Demographics, service usage, billing info, contract types

---

## 🧠 Machine Learning Models Used

| Model           | Cross-Validation Accuracy |
|-----------------|---------------------------|
| Decision Tree   | 78%                        |
| XGBoost         | 83%                        |
| ✅ Random Forest | **84%** (Best Performer)   |

---

## 🔍 Project Workflow

1. **Data Cleaning**
   - Removed irrelevant column `customerID`
   - Handled blank values in `TotalCharges`
   - Converted columns to appropriate data types

2. **Exploratory Data Analysis (EDA)**
   - Histograms, boxplots, and countplots for insights
   - Identified key features contributing to churn

3. **Data Preprocessing**
   - Label-encoded categorical features
   - Used **SMOTE** to handle class imbalance

4. **Model Training**
   - Trained Decision Tree, Random Forest, and XGBoost
   - Evaluated with 5-fold cross-validation

5. **Model Deployment**
   - Saved model as `customer_churn_model.pkl`
   - Saved encoders as `encoders.pkl`
   - Built an interactive user-input prediction system

---

## 🧾 Sample Input for Prediction

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
encoders.pkl	Saved label encoders for prediction
Telco-Customer-Churn.csv	Dataset used for training

🛠 Technologies Used
Python (Pandas, NumPy)

Scikit-learn

XGBoost

imbalanced-learn (SMOTE)

Seaborn & Matplotlib (for EDA)

Pickle (model serialization)

Google Colab

🚀 Future Enhancements
Add hyperparameter tuning using GridSearchCV / Optuna

Integrate explainability with SHAP / LIME

Deploy as a web application using Streamlit or Flask

Integrate with real-time churn monitoring pipelines

👩‍💻 Author
Subhadra Bhattacharyya
Aspiring Data Scientist | Machine Learning Enthusiast

