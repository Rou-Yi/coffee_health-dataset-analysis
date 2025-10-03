# Global Coffee and Health Data Analysis & Classification

This repository explores the Kaggle dataset [**Global Coffee Health Dataset**](https://www.kaggle.com/datasets/uom190346a/global-coffee-health-dataset) that includes 10,000 synthetic records reflecting real-world patterns of coffee consumption, sleeping, and health outcomes across 20 countries.  

The project aims to:  
- Use **data visualization** to explore potential relationships between health status, sleep patterns, and habits (e.g., smoking).
- Develop **classification models** for predicting **Health Issues** and **Stress Levels**.

---

## Methodology Overview
1. **Exploratory Data Analysis (EDA)**
   - Checking data types and dealing with missing values
   - Histograms and bar charts for quantitative features
   - Heatmaps for categorical associations
   - Investigating key relationship with **Health Issues** and **Stress Levels**

2. **Feature Engineering**
   - Dropping irrelevant variables (`Caffeine_mg`, `Sleep_Quality`, `Country`) 
   - Encoding categorical features (e.g., label encoding and one-hot encoding)
   - Scaling numerical features

3. **Machine Learning Model**
   - Train/Test split (60% Train, 40% Test)
   - Training a **random forest classifier** for **Health Issues** and **Stress Levels**
   - Feature importance analysis

---

## Results / Key Findings
### Model Performance Summary

| Model Scope | Health Issue Accuracy | Stress Level Accuracy | Insight |
| :--- | :--- | :--- | :--- |
| All 20 Features | 98.12% | 97.90% | Baseline performance is strong, with high feature count. |
| Top 3 Features Only | **98.50%** | 98.00% | Simplified model **outperforms** the full model. |

### Key Observations & Feature Importance

1.  **Model Simplification Improves Performance:**
    The model trained using only the **Top 3 Features** not only achieved a slightly higher overall accuracy (**98.50%** vs. **98.12%**) but also significantly improved the robustness of specific classifications. The **F1-score for Class 3 (Severe) Health Issue improved from 25% to 100%** (though based on only 7 test cases), indicating the simplified model's efficiency and targeted improvement.

2.  **Dominance of Sleep Duration:**
    **Sleep Hours** remains the feature of paramount importance across both classification tasks, as shown in the feature importance charts below. This finding indicates the **strong influence of sleep on both overall health status and stress levels.**

3.  **Feature Importance Visuals:**
    The feature importance charts for the full models are shown below:

| Health Model Feature Importance | Stress Model Feature Importance |
| ------------ | ------------ |
| <img width="865" height="379" alt="image" src="https://github.com/user-attachments/assets/28139e67-392f-43c8-9cab-51e07caaa45e" /> | <img width="856" height="379" alt="image" src="https://github.com/user-attachments/assets/fb0b616c-f073-4d04-b9a7-e14aa54a3619" /> |
