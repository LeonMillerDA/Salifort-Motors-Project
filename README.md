# 🚀 Employee Churn Prediction - Salifort Motors

Predicting which employees are likely to leave Salifort Motors using **Random Forest classification**, with actionable insights to improve retention.  

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](YOUR_NOTEBOOK_LINK)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 📌 Table of Contents
1. [Project Overview](#project-overview)  
2. [Dataset](#dataset)  
3. [Exploratory Data Analysis](#exploratory-data-analysis)  
4. [Modeling](#modeling)  
5. [Evaluation Metrics](#evaluation-metrics)  
6. [Feature Importance](#feature-importance)  
7. [Results](#results)  
8. [Conclusion & Recommendations](#conclusion--recommendations)  
9. [Next Steps](#next-steps)  
10. [License](#license)  

---

## 📝 Project Overview
- **Problem:** HR wants to reduce employee turnover by understanding factors that lead employees to leave.  
- **Goal:** Build a predictive model to identify employees likely to leave and provide actionable recommendations.  
- **Target Variable:** `left` (1 = left, 0 = stayed)

---

## 📊 Dataset
- **Source:** [Kaggle - HR Analytics and Job Prediction](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction/data)  
- **Rows:** 14,999 | **Columns:** 10  
- **Key Features:**  
  - Satisfactory Level  
  - Number of Projects  
  - Average Monthly Hours  
  - Time Spent in Company  
  - Promotion Last 5 Years  
  - Department  
  - Salary  
  - Last Evaluation  

---

## 🔍 Exploratory Data Analysis
- Checked for missing values and duplicates ✅  
- Cleaned column names and handled outliers  
- Target distribution:  
  - Stayed: 76%  
  - Left: 24%  
- Correlation heatmap highlights relationships among features  

![Correlation Heatmap](images/correlation_heatmap.jpg)  

---

## 🛠 Modeling
- **Model:** Random Forest Classifier  
- **Data Preparation:**  
  - Dummy encoding / ordinal encoding for categorical variables  
  - Removed `satisfactory level` to reduce target leakage  
- **Primary Metric:** ROC AUC  

---

## 📈 Evaluation Metrics
| Metric     | Score |
|------------|-------|
| AUC        | 94.2% |
| Precision  | 90.9% |
| Recall     | 90.3% |
| F1-Score   | 90.6% |
| Accuracy   | 96.8% |

- **Confusion Matrix:**  
![Confusion Matrix](images/confusion_matrix.jpg)  

- **ROC Curve:**  
![ROC Curve](images/roc_curve.jpg)  

---

## 🌟 Feature Importance
Most impactful features (after removing `satisfactory level`):  
1. Average Monthly Hours  
2. Tenure (Time Spent in Company)  
3. Number of Projects  
4. Last Evaluation  

![Feature Importance](images/feature_importance.jpg)  

---

## ✅ Results
- Random Forest achieved high predictive performance across all metrics  
- Workload and tenure are key factors influencing employee churn  
- Removing `satisfactory level` reduced bias and confirmed actionable insights  

---

## 💡 Conclusion & Recommendations
- Limit the number of projects assigned to employees  
- Adjust expectations or reward employees for working long hours  
- Promote employees with ≥4 years tenure or investigate dissatisfaction factors  

---

## 🔮 Next Steps
- Explore tree-based ensemble models like XGBoost or LightGBM  
- Investigate additional engagement factors not included in current dataset  
- Build an **interactive dashboard** to monitor employee churn risk in real-time  

---

## 📜 License
MIT License
