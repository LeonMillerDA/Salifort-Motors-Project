# 🚦 Predicting Employee Turnover at Salifort Motors | Decision Tree & Random Forest
**Accuracy:** **97.8%** ✅ | **AUC:** **98%** 🚀

Predict which employees are likely to leave Salifort Motors using tree-based classification models, with actionable insights to improve retention.

---

## 📌 Table of Contents

- [Project Overview](#project-overview)  
- [Dataset](#dataset)  
- [Exploratory Data Analysis](#exploratory-data-analysis)  
- [Model Comparison](#model-comparison)  
- [Evaluation Metrics](#evaluation-metrics)  
- [Results & Key Features](#results--key-features)  
- [Visualizations](#visualizations)  
- [Conclusion & Recommendations](#conclusion--recommendations)  
- [Next Steps](#next-steps)

---

## 📝 Project Overview
---
**Problem:** High employee turnover is costly, leading to lost productivity and recruitment expenses.  

**Goal:** Predict which employees are at risk of leaving and identify actionable factors driving attrition.  

**Target Variable:** `left` (1 = left, 0 = stayed)  

**Business Impact:** Early identification of at-risk employees allows management to implement retention strategies, saving costs and improving workforce stability.

---

## 📊 Dataset
---
**Source:** [Kaggle – HR Analytics & Job Prediction](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction/data)  

**Shape:** 14,999 rows × 10 columns  

**Feature Types:**  
- **Numerical:** Satisfaction Level, Number of Projects, Average Monthly Hours, Tenure, Employee Review Score  
- **Categorical:** Department, Salary, Promotion in Last 5 Years  

**Key Features:**  
- Satisfaction Level  
- Number of Projects  
- Average Monthly Hours  
- Tenure  
- Promotion in Last 5 Years  
- Department  
- Salary  
- Employee Review Score  

---

## 🔍 Exploratory Data Analysis
---
- No missing values ✅  
- Duplicates removed, column names cleaned  
- Outliers explored in tenure  

**Target distribution:**  
- **Stayed:** 83.4% | **Left:** 16.6%  

📌 **Insight:** The dataset is imbalanced. Metrics like **AUC** and **F1-score** are more reliable than accuracy alone.

---

## 🛠 Model Comparison
---
| Model | Precision | Recall | F1-Score | Accuracy | AUC | Notes |
|-------|-----------|--------|----------|---------|-----|-------|
| Decision Tree (CV) | 0.916 | 0.917 | 0.916 | 0.972 | 0.970 | Cross-validated on training set |
| Random Forest (CV) | 0.950 | 0.916 | 0.933 | 0.978 | 0.980 | ✅ Chosen final model |

✅ **Random Forest** was selected for its **high AUC**, strong generalization, and ability to capture feature interactions effectively.

---

## 📈 Evaluation Metrics
---
**Random Forest – Test Data**  

- 🔹 **Precision:** 0.909  
- 🔹 **Recall:** 0.904  
- 🔹 **F1-Score:** 0.906  
- 🔹 **Accuracy:** 0.969  
- 🔹 **AUC:** 0.943  

📌 **Insight:** Excellent **discrimination** between employees who stay vs. leave — the model effectively ranks employees by risk.

---

## ✅ Results & Key Features
---
**Top Features Driving Attrition:**  
1. **Number of Projects**  
2. **Average Monthly Hours**  
3. **Employee Review Score**  
4. **Tenure**  

📌 **Summary:** Workload, tenure, project count, and review scores are the main drivers of employee churn. Targeting these areas can significantly reduce turnover.

---

## 🖼 Visualizations
---

### Correlation Heatmap
<img src="images/correlation_heatmap.jpg" alt="Correlation Heatmap" width="400"/>  
*Shows feature relationships and potential multicollinearity.*

### Feature Importance
<img src="images/feature_importance.jpg" alt="Feature Importance" width="400"/>  
*Number of projects and workload metrics are strongest predictors.*

### ROC Curve
<img src="images/roc_curve.jpg" alt="ROC Curve" width="400"/>  
*High AUC → excellent discrimination between employees who stay vs. leave.*

---

## 💡 Conclusion & Recommendations
---
- **Optimize project assignments** to prevent overload.  
- **Recognize & reward high-hour employees** to reduce burnout.  
- **Investigate dissatisfaction among employees with ≥4 years tenure**; consider promotions or retention programs.

---

## 🔮 Next Steps
---
- Explore **boosting methods** like XGBoost or LightGBM for potential performance gains.  
- Incorporate **external engagement/survey data** for richer features.  
- Build a **real-time dashboard** for managers to monitor churn risk.  
- Deploy models to enable predictive HR analytics across departments.
