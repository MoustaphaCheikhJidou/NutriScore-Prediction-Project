# NutriScore Prediction Project

This project leverages machine learning to predict the NutriScore of food products based on their nutritional composition. Using the Open Food Facts dataset, we applied various supervised learning algorithms to classify products into NutriScore categories (A to E) and identify key nutrients influencing these scores.

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Business Understanding](#business-understanding)
4. [Machine Learning Models](#machine-learning-models)
5. [Results](#results)
6. [How to Run](#how-to-run)
7. [Files Included](#files-included)
8. [License](#license)

---

## Project Overview
NutriScore is a scoring system designed to guide consumers in evaluating the nutritional quality of food products. This project:
- Predicts NutriScore categories using nutritional attributes like energy, fats, sugar, and fiber content.
- Identifies significant features influencing NutriScore classification.
- Compares and evaluates various machine learning models for performance and interpretability.

---

## Dataset
The dataset was sourced from [Open Food Facts](https://world.openfoodfacts.org/), a public database providing detailed information about food products. Key features include:
- Nutritional composition (e.g., energy, fats, sugar, protein).
- Product metadata (e.g., name, brands, packaging).
- Categorization tags and NutriScore labels.

---

## Business Understanding
### Context
This project aims to develop an automated system for predicting NutriScore labels based on food product nutrients. The goal is to provide consumers and producers with a tool for improving the nutritional quality of their products.

### Primary Problem:
- Can NutriScore categories be predicted using only declared nutrient data?

### Secondary Questions:
1. Which nutrients have the most impact on NutriScore classification?
2. How can products be categorized into specific microeconomic groups (e.g., beverages, fats)?

---

## Machine Learning Models
The following supervised learning models were implemented and evaluated:
1. **Logistic Regression**: Achieved 75% accuracy with an AUC of 0.9378. A simple yet interpretable baseline model.
2. **Random Forest**: Improved results with 87% accuracy and an AUC of 0.9788, leveraging non-linear interactions.
3. **K-Nearest Neighbors (KNN)**: Achieved 81% accuracy with an AUC of 0.9652. Sensitive to data quality but performed well after tuning.
4. **XGBoost**: The best-performing model with 89% accuracy and an AUC of 0.9855, thanks to efficient hyperparameter optimization.

---

## Results
The table below summarizes the key performance metrics for each model:

| Model              | Accuracy | AUC (Macro Avg) |
|---------------------|----------|-----------------|
| Logistic Regression | 75%      | 0.9378          |
| Random Forest       | 87%      | 0.9788          |
| KNN                 | 81%      | 0.9652          |
| XGBoost             | 89%      | 0.9855          |

### Key Insights:
- Nutrients like fat, sugar, and fiber significantly influence NutriScore.
- XGBoost and Random Forest outperformed others, with XGBoost providing the most robust and precise results.

---

## How to Run
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/NutriScore-Prediction-Project.git
   cd NutriScore-Prediction-Project
