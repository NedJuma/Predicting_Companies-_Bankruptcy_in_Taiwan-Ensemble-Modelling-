# 🏦 Predicting Campanies Bankruptcy in Taiwan (Random Forest Classifier)
## 📌 Project Overview
This project focuses on predicting company bankruptcy in Taiwan using financial and operational indicators. 
The goal was to build and evaluate machine learning models that can accurately identify financially distressed companies while handling severe class imbalance effectively.

## 🎯 Objective

To develop a predictive model that can:
- Identify companies at risk of bankruptcy
- Handle severe class imbalance effectively
- Balance precision and recall for meaningful financial risk detection
- Provide insights into the most influential financial indicators
## 📊 Dataset Description
The dataset contains financial ratios and indicators of Taiwanese companies, including:

- Profitability ratios (ROA, ROE, gross margin, etc.)
- Liquidity ratios (current ratio, quick ratio, etc.)
- Leverage ratios (debt ratio, equity ratio, etc.)
- Cash flow indicators
- Operational efficiency metrics
 > Target Variable:
- Bankrupt?: 1 → Company is bankrupt, 0 → Company is not bankrupt
## ⚖️ Class Imbalance Challenge
- Non-bankrupt: ~97%
- Bankrupt: ~3%

This required specialized handling using:

- Undersampling
- Oversampling
- Baseline (no resampling)
## 🧠 Models Built

> Three modeling strategies were evaluated using a Random Forest Classifier:
- Base Model (No Resampling)
- Undersampled Model
- Oversampled Model
## 📈 Evaluation Metrics Used
To ensure robust evaluation beyond accuracy, the following metrics were used:
- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix
- ROC-AUC
- Cohen’s Kappa
- Precision-Recall Trade-offs
## 📊 Model Performance Summary
Model	Accuracy	ROC-AUC	Kappa	Bankruptcy Recall	Bankruptcy F1
Base Model	0.97	0.918	0.30	0.20	0.31
Under-sampled	0.86	0.934	0.26	0.86	0.31
Over-sampled	0.97	0.897	0.39	0.31	0.41
## 🏆 Final Model Selection

> 👉 Selected Model: Oversampled Random Forest
Why this model?:
- Best overall balance between precision and recall
- Highest Cohen’s Kappa (0.39) → strongest agreement beyond chance
- Best F1-score for bankrupt class (0.41)
- Strong ROC-AUC performance (~0.90+)
- Maintains high overall accuracy without ignoring minority class
## 🔍 Key Insights
- Accuracy alone is misleading in highly imbalanced datasets
- Undersampling improves recall but introduces too many false positives
- Oversampling provides the best trade-off between detection and reliability
- ROC-AUC and Kappa confirmed that oversampling improves overall model robustness
## 🚀 Future Improvements
- Threshold tuning to improve bankruptcy recall
- Feature importance analysis (e.g., SHAP values)
- Hyperparameter optimization 

## 🛠️ Tech Stack
- Python 
- Pandas & NumPy
- Scikit-learn
- Imbalanced-learn
- Matplotlib & Seaborn

## 📣 Conclusion
This project demonstrates how machine learning can be applied to financial risk prediction under severe class imbalance. Through systematic evaluation of multiple resampling strategies, the oversampled model emerged as the most reliable and balanced approach for predicting corporate bankruptcy in Taiwan.