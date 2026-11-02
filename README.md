# 🏥 Healthcare No-Show Prediction

## 📌 Overview
Missed medical appointments (no-shows) lead to inefficient use of healthcare resources and increased operational costs.

This project aims to predict whether a patient will miss their appointment and analyze key factors influencing no-show behavior.

---

## 🎯 Objectives

- Predict patient no-shows using machine learning
- Identify key factors affecting appointment attendance
- Minimize **false negatives** (missed risky patients)
- Extract actionable insights from patient data

---

## 📁 Project Structure

```
healthcare-no-show-prediction/
├── data/
│   ├── raw/
│   │   └── medical_appointment_no_show_raw.csv
│   └── processed/
│       ├── medical_appointment_no_show_cleaned.csv
│       └── final_model_dataset.csv
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_quality_checks.ipynb
│   ├── 03_eda_no_show.ipynb
│   ├── 04_feature_engineering.ipynb
│   └── 05_model_evaluation_error_analysis.ipynb
├── journey.txt
└── README.md
```

---

## ⚙️ Workflow

### 1. Data Understanding
- Explored dataset structure and feature meanings
- Identified target variable (`No-show`)

### 2. Data Quality Checks
- Handled invalid values (e.g., negative age)
- Fixed inconsistencies in features
- Created `WaitingDays` feature from date columns

### 3. Exploratory Data Analysis (EDA)
- Analyzed distribution of no-show cases
- Studied relationships between features and target variable
- Visualized patterns using plots

### 4. Feature Engineering
- Converted categorical variables into numerical format
- Removed irrelevant features (e.g., high-cardinality columns)
- Prepared dataset for model training

### 5. Model Building
- Logistic Regression (primary model)
- Random Forest (comparison model)

### 6. Model Evaluation
- Metrics used:
  - Accuracy
  - Precision
  - Recall
  - Confusion Matrix
  - ROC-AUC Score

- Focused on **Recall**, as missing risky patients is critical

### 7. Threshold Tuning
- Adjusted classification threshold to improve recall
- Reduced false negatives (missed no-show patients)

### 8. Error Analysis
- Analyzed False Positives and False Negatives
- Compared patterns between correctly and incorrectly predicted cases
- Added visualizations for better understanding

---

## 📊 Key Insights

- Patients with **longer waiting times** are more likely to miss appointments  
- The model performs better for **younger patients**  
- **Older patients are often misclassified**  
- **SMS reminders showed no clear reduction in no-shows.** 

---

## 📈 Results

- Accuracy: ~60%  
- Recall (No-show class): Improved using threshold tuning  
- AUC Score: ~0.54  

The model shows moderate predictive performance but provides meaningful behavioral insights.

---

## 🧠 Key Learnings

- Accuracy is not reliable for **imbalanced datasets**
- Recall is critical when detecting high-risk cases
- Threshold tuning can significantly impact model performance
- Error analysis is essential to understand model limitations

---

## 🚀 Future Improvements

- Apply advanced models (XGBoost, Gradient Boosting)
- Handle class imbalance using resampling techniques
- Deploy model using Streamlit for interactive dashboard

---

## 📌 Project Status

✅ Completed  
✅ Structured and documented  
 

---

## 🤝 Acknowledgement

This project was built as part of a self-learning journey to understand 
end-to-end machine learning workflows and real-world problem solving.
