# 🚦 Predicting Employee Turnover at Salifort Motors | Decision Tree & Random Forest | AUC 98%, Accuracy 97.8%

Predicting which employees are likely to leave Salifort Motors using tree-based classification models, with actionable insights to improve retention.

## 📌 Table of Contents

- **[📝 Project Overview](#project-overview)**  
- **[📊 Dataset](#dataset)**  
- **[🔍 Exploratory Data Analysis](#exploratory-data-analysis)**  
- **[🛠 Model Comparison](#model-comparison)**  
- **[📈 Evaluation Metrics](#evaluation-metrics)**  
- **[✅ Results & Key Features](#results--key-features)**  
- **[🖼 Visualizations](#visualizations)**  
- **[💡 Conclusion & Recommendations](#conclusion--recommendations)**  
- **[🔮 Next Steps](#next-steps)**

## 📝 Project Overview
---
**Problem:** High employee turnover is costly. Salifort Motors wants to identify which employees are most at risk of leaving.  

**Goal:** Build predictive models to forecast attrition and uncover key drivers behind employee churn.  

**Target Variable:** `left` (1 = left, 0 = stayed)

## 📊 Dataset
---
**Source:** Kaggle - HR Analytics and Job Prediction  

**Shape:** 14,999 rows × 10 columns  

**Key Features:**  
- Satisfaction Level  
- Number of Projects  
- Average Monthly Hours  
- Tenure (time_spend_company)  
- Promotion in Last 5 Years  
- Department  
- Salary  
- Last Evaluation  

## 🔍 Exploratory Data Analysis
---
- No missing values were found ✅  
- Duplicates removed, column names cleaned  
- Outliers explored in tenure  

**Target distribution:**  
- Stayed: 83.4%  
- Left: 16.6%  

📌 **Insight:** The dataset is imbalanced, with a majority of employees staying.

## 🛠 Model Comparison
---
| Model | Precision | Recall | F1-Score | Accuracy | AUC | Notes |
|-------|-----------|--------|----------|---------|-----|-------|
| Decision Tree (CV) | 0.9155 | 0.9169 | 0.9157 | 0.9719 | 0.9698 | Cross-validated on training set |
| Random Forest (CV) | 0.9500 | 0.9156 | 0.9325 | 0.9779 | 0.9804 | Chosen final model |

✅ Random Forest was chosen as the final model due to higher AUC and accuracy.

## 📈 Evaluation Metrics
---
**Random Forest – Test Data**  

| Metric | Score |
|--------|-------|
| Precision | 0.9091 |
| Recall | 0.9036 |
| F1-Score | 0.9063 |
| Accuracy | 0.9689 |
| AUC | 0.9428 |

## ✅ Results & Key Features
---
**Top Features Influencing Attrition:**  

| Rank | Feature |
|------|--------|
| 1 | 🔹 Number of Projects |
| 2 | 🔹 Average Monthly Hours |
| 3 | 🔹 Employee Review Score |
| 4 | 🔹 Tenure  |

📌 **Summary:** Random Forest achieved strong performance on the test set. Workload, tenure, project count, and review scores are the main drivers of employee churn.

## 🖼 Visualizations
---

### Correlation Heatmap
<img src="images/correlation_heatmap.jpg" alt="Correlation Heatmap" width="400"/>

### Feature Importance
<img src="images/feature_importance.jpg" alt="Feature Importance" width="400"/>

### ROC Curve
<img src="images/roc_curve.jpg" alt="ROC Curve" width="400"/>

## 💡 Conclusion & Recommendations
---
- Limit the number of projects assigned to employees.  
- Adjust expectations or reward employees for long working hours.  
- Consider promoting employees with ≥4 years tenure or investigate dissatisfaction patterns at that stage.

## 🔮 Next Steps
---
- Explore boosting methods like XGBoost or LightGBM for potential gains.  
- Incorporate external engagement or survey data for richer features.  
- Build an interactive dashboard to monitor employee churn risk in real-time.
