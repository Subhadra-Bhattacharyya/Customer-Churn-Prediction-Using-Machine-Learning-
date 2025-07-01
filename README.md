# 📉 Customer Churn Prediction using Machine Learning

This project predicts whether a customer is likely to **churn (leave the telecom service)** using historical customer behavior and contract data. It applies **SMOTE**, **machine learning models**, and **user-interactive forecasting** to support proactive retention strategies.

---

## 🚀 Project Objectives

- Analyze customer service, demographic, and billing data  
- Handle class imbalance using **SMOTE**  
- Train multiple ML models for churn classification  
- Build an interactive system for churn prediction using custom input  
- Save and reuse model and encoders using `pickle`

---

## 🧾 Dataset Overview

- **Source**: IBM Sample — Telco Customer Churn Dataset  
- **Records**: 7,043 customers  
- **Target Column**: `Churn` (Yes/No)  
- **Features**: Demographics, service plans, payment methods, tenure, charges, etc.

---

## 🧠 Models Used

| Model            | Accuracy (CV) |
|------------------|---------------|
| Decision Tree    | 78%           |
| XGBoost          | 83%           |
| ✅ Random Forest | **84%**       |

> ✅ Random Forest was selected for final deployment due to its strong performance and generalization.

---

## ⚙️ Technologies

- Python (Google Colab)  
- Libraries: `pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn`, `xgboost`, `imbalanced-learn`  
- Tools: `LabelEncoder`, `SMOTE`, `cross_val_score`, `pickle`

---

## 🧪 Methodology

1. **Data Preprocessing**  
   - Dropped non-informative columns like `customerID`  
   - Handled blank values in `TotalCharges`, converted to float  
   - Encoded categorical variables  
   - Used **SMOTE** to balance the target class

2. **Exploratory Data Analysis (EDA)**  
   - Count plots, histograms, box plots  
   - Time-independent feature distribution  
   - Heatmap for numerical correlations

3. **Model Training**  
   - Applied 3 models: Decision Tree, Random Forest, XGBoost  
   - Evaluated using 5-fold cross-validation and accuracy

4. **Deployment**  
   - Saved trained model (`.pkl`) and encoders  
   - Built a dynamic user input system to predict churn status

---

## 👤 User Input Example

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
📈 Model Evaluation
Metric	Score
Accuracy	77.8%
Precision	58%
Recall	59%
F1 Score	58%

📁 Project Structure
File	Description
Churn_Prediction.ipynb	Full Colab notebook (EDA + ML)
customer_churn_model.pkl	Trained Random Forest model
encoders.pkl	Saved encoders for label mapping
Telco-Customer-Churn.csv	Dataset used for training

📌 Features
📊 Interactive prediction system

✅ Class imbalance solved using SMOTE

🔁 Model & encoder reuse with pickle

🧠 Predicts churn likelihood based on real customer profiles

✅ Conclusion
This project demonstrates a practical machine learning solution for customer churn prediction. By leveraging class balancing, ensemble models, and real-world user inputs, it helps telecom companies act before losing customers.

🤝 Contributing
Open to contributions:

Model hyperparameter tuning (GridSearchCV, Optuna)

SHAP or LIME integration for explainability

Streamlit/Flask deployment

Dashboard-based visualization

📬 Contact
Author: Subhadra Bhattacharyya
📧 Email: subhadrabhattacharyya7@gmail.com
🌐 Location: India

