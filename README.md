# Retail Customer Response Prediction | R & Machine Learning

## Project Overview

This project investigates whether historical customer demographics and purchasing behaviour can be used to predict whether a household will participate in a retail marketing campaign.

The project was completed as part of a Master's dissertation in Business Analytics using the Dunnhumby "The Complete Journey" dataset.

The analysis covers the full workflow from data preparation and feature engineering to classification model comparison, tuning, and evaluation.

## Business Problem

Retailers need to decide which customers are more likely to respond to marketing campaigns.

The objective of this project was to investigate whether customer characteristics and purchasing behaviour could be used to predict campaign participation and support more targeted marketing decisions.

## Dataset

The analysis uses Dunnhumby's "The Complete Journey" dataset, which contains household-level transaction, demographic, product, and campaign information collected over approximately two years.

The repository includes the original dataset user guide. The dataset itself is not included in this repository.

## Analytical Workflow

The analysis followed these main stages:

1. Data cleaning and validation
2. Integration of demographic, transaction, product, and campaign data
3. Customer-level feature engineering
4. Handling class imbalance using SMOTE
5. Feature selection and dimensionality reduction
6. Comparison of multiple classification algorithms
7. Model tuning using cross-validation
8. Test-set evaluation
9. Interpretation of model performance for different marketing objectives

## Key Features

Customer-level predictors included:

- Demographic characteristics
- Average basket value
- Weekly spending
- Total shopping trips
- Shopping frequency
- Transaction timing
- Frequently purchased products

The target variable represented whether a household participated in the marketing campaign.

## Models Evaluated

Multiple classification algorithms were initially compared.

Three ensemble models were selected for further evaluation:

- Random Forest
- Boosted C5.0 Decision Tree
- Bagged Decision Tree

## Model Results

Performance was evaluated using sensitivity, specificity, accuracy, balanced accuracy, and ROC/AUC.

| Model | Sensitivity | Specificity | Accuracy | Balanced Accuracy | AUC |
|---|---:|---:|---:|---:|---:|
| Random Forest (tuned) | 91.1% | 63.7% | 67.9% | 77.4% | ~0.81 |
| Boosted C5.0 (default) | 83.1% | 87.5% | 86.8% | 85.3% | ~0.92 |
| Bagged Decision Tree (tuned) | 87.9% | 69.1% | 72.1% | 78.5% | Not numerically reported |

### Interpretation

The models showed different performance trade-offs.

- Random Forest achieved the highest sensitivity, identifying a larger proportion of potential participants.
- Boosted C5.0 achieved higher specificity and the highest reported AUC among the selected models.
- Bagged Decision Tree provided an intermediate trade-off between sensitivity and specificity.

The analysis therefore considered model selection in relation to the business objective rather than relying on a single performance metric.

## Key Findings

The analysis suggests that demographic characteristics, purchasing behaviour, and product-related information can provide useful predictors of campaign participation.

The results also demonstrate the importance of considering the relative consequences of false positives and missed potential participants when selecting a classification model.

## Limitations

The project has several limitations:

- The analysis is based on a single retail dataset.
- The available variables represent only a subset of the factors that may influence campaign participation.
- The models predict likelihood of participation rather than the magnitude of customer response.
- Results may not generalise directly to different retailers, campaigns, or time periods.

## Future Research

Potential extensions include:

- Incorporating additional customer and behavioural variables
- Testing the models across different campaigns or time periods
- Investigating model interpretability and feature importance
- Exploring cost-sensitive modelling using actual campaign costs
- Evaluating generalisation on additional datasets

## Repository Contents

- `dunnhumby.R` — R source code for data preparation, analysis, modelling, and evaluation
- `Application of data mining and machine learning in retail marketing.docx` — Master's dissertation
- `dunnhumby - The Complete Journey User Guide.pdf` — Dataset documentation
- `README.md` — Project documentation

## Dataset

The analysis uses Dunnhumby's "The Complete Journey" dataset, which contains household-level transaction, demographic, product, and campaign information collected over approximately two years.

The dataset can be downloaded from Kaggle:

**[Download the Dunnhumby "The Complete Journey" dataset](https://www.kaggle.com/datasets/frtgnn/dunnhumby-the-complete-journey)**

The repository includes the original dataset user guide. The dataset itself is not included in this repository.

## Tools & Methods

**R · RStudio · Data Mining · Machine Learning · Classification ·
Feature Engineering · SMOTE · Cross-Validation · Model Evaluation**

## Academic Context

Master's dissertation in Business Analytics.

This repository contains the original project materials and analysis code from the dissertation.
