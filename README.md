https://www.kaggle.com/datasets/pratyushpuri/used-car-sales-listings-dataset-2025

# Used_cars_sales_listing_dataset_Analyzing
🚗 Used Car Price Prediction with Machine Learning   End-to-end ML pipeline for predicting used car prices using Python (scikit-learn).   Includes data preprocessing, feature engineering, model training, and evaluation.   Best model: Gradient Boosting (R² = 0.94, RMSE ≈ 2,334).
# 🚗 Used Car Price Prediction

This project builds a machine learning pipeline to predict **used car prices** based on various attributes such as year, mileage, make, model, body type, condition, and features.

## 📌 Project Overview
- Dataset: **2,068 used car listings**  
- Goal: Predict **car price** from specifications  
- Steps:
  1. Data Cleaning & Missing Value Handling
  2. Encoding Categorical Variables
  3. Feature Engineering (multi-hot encoding for features)
  4. Train-Test Split & Scaling
  5. Model Training (Linear Regression, Random Forest, Gradient Boosting)
  6. Performance Comparison

## ⚙️ Data Preprocessing
- Filled missing values:
  - `trim` → `"Unknown"`
  - `condition` → `"Unknown"`
  - `features` → `"None"`
- Label Encoding for high-cardinality categorical features (`make`, `model`, `location`, `trim`)
- One-Hot Encoding for low-cardinality features (`fuel_type`, `transmission`, `body_type`, `condition`, `seller_type`)
- MultiLabelBinarizer applied to `features` column

## 📊 Models & Results
| Model              | R² Score | RMSE    |
|--------------------|----------|---------|
| Linear Regression  | 0.62     | ~6,032  |
| Random Forest      | 0.84     | ~3,927  |
| Gradient Boosting  | **0.94** | **~2,334** |

✅ **Gradient Boosting** delivered the best performance, explaining **94% of variance** in car prices with the lowest prediction error.

## 🔑 Key Insights
- **Year** and **Mileage** are the most important predictors of car prices.
- **Brand (Make)**, **Model**, **Condition**, and **Features** also significantly influence pricing.
- Advanced models (Boosting) outperform linear models due to non-linear relationships and categorical complexity.

## 🚀 Tech Stack
- **Python 3**
- **Libraries:** pandas, numpy, scikit-learn, matplotlib, seaborn

## 📂 Project Structure
