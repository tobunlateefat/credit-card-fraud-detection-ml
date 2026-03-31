# A Comparative Analysis of Machine Learning Algorithms for Detecting Credit Card Fraud as a Financial Crime

## Overview
Credit card fraud is a growing financial crime causing significant losses globally. According to the UK Finance Annual Fraud Report (2022), £1.2 billion in fraud losses were recorded with over 2.9 million verified cases — with unauthorised payment card fraud alone estimated at £726.9 million. This project applies and compares machine learning algorithms to detect fraudulent transactions, addressing a critical gap in existing research.

## Research Aim
To explore a comparison of machine learning algorithms for credit card fraud detection and identify the most efficient algorithm for real-time fraud prediction.

## Research Objectives
- Review existing machine learning algorithms for credit card fraud prediction
- Identify the most efficient machine learning algorithm for fraud detection
- Assess the interaction of various machine learning algorithms on credit card fraud data

## Research Questions
- Can machine learning improve credit card fraud prediction?
- To what extent can machine learning detect credit card fraud?
- Which machine learning algorithm detects credit card fraud with the highest accuracy?

## Dataset
- Source: [Kaggle Credit Card Fraud Detection Dataset](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)
- 284,807 real credit card transactions from European cardholders
- Only 0.17% are fraudulent — reflecting the real-world class imbalance challenge
- Features V1-V28 are anonymised via PCA to protect cardholder privacy

## Problem Statement
Most existing studies examine machine learning algorithms individually. This project fills that gap by conducting a direct comparative analysis, helping financial institutions make informed, data-driven decisions about fraud prevention systems.

## Methodology
- Exploratory Data Analysis (EDA)
- Data preprocessing and feature scaling (StandardScaler)
- Class imbalance handling using SMOTE (Synthetic Minority Oversampling Technique)
- 80/20 train-test split with stratification
- Model training, evaluation and comparison

## Results

| Model | Fraud Precision | Fraud Recall | Fraud F1-Score | ROC-AUC |
|-------|----------------|--------------|----------------|---------|
| Logistic Regression | 0.06 | 0.92 | 0.11 | 0.95 |
| Random Forest | 0.87 | 0.83 | 0.85 | 0.91 |

## Key Findings
- Random Forest significantly outperforms Logistic Regression in overall fraud detection quality, achieving an F1-score of 0.85 vs 0.11
- Logistic Regression achieves higher recall but generates excessive false alarms, making it impractical for real-world deployment
- Random Forest correctly identified 81 out of 98 fraud cases with only 12 false alarms across 56,864 legitimate transactions
- SMOTE was critical in addressing class imbalance — balancing 394 fraud cases against 227,451 legitimate ones in the training set

## Conclusion
Random Forest delivers the best balance between precision and recall for real-world fraud detection. In a production banking environment, minimising false alarms while maintaining high fraud detection rates is essential to both operational efficiency and customer trust.

## Tools & Libraries
Python, Pandas, NumPy, Scikit-learn, Imbalanced-learn, Matplotlib, Seaborn

## Academic Context
This project is based on original MSc dissertation research supervised by Dr. Ashima Chopra at the University of Bradford (2023–2024).

## Author
**Lateefat Tobun** — MSc Applied AI & Data Analytics (Distinction), University of Bradford
