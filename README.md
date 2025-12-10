# Data_Preprocessing
# Toyota Dataset Preprocessing Project

## Project Overview
This project focuses on **preprocessing the Toyota dataset** to make it ready for machine learning modeling. The dataset contains information about Toyota cars, including specifications such as price, age, kilometers driven, fuel type, horsepower, metallic color, transmission type, engine capacity, number of doors, and weight.  

The goal of this project is to **clean, transform, and reduce the dataset** to retain only the most relevant features for predicting car prices.

---

## Dataset Information
- **Source:** Kaggle Toyota Dataset  
- **Number of records:** 1436  
- **Number of features:** 11 (originally)  
- **Target variable:** `Price`  
- **Feature types:** Numeric and categorical  

**Selected Features after Preprocessing:**  
- `Age` – Age of the car  
- `Weight` – Weight of the car  
- `MetColor` – Metallic color (1 = Yes, 0 = No)  

The rest of the features were removed due to low predictive power or redundancy.

---

## Preprocessing Steps

### 1. Data Cleaning
- Removed unnecessary columns such as `Unnamed: 0`.
- Handled missing values in `Age`, `FuelType`, and `MetColor` using median imputation.
- Converted object-type columns (e.g., `KM`, `HP`, `Doors`) to numeric types.

### 2. Feature Selection (Dimensionality Reduction)
- **Recursive Feature Elimination (RFE):** Selected the top features based on Linear Regression.
- **Random Forest Feature Importance:** Ranked features by predictive power.
- Retained only the most relevant features: `Age`, `Weight`, `MetColor`.

### 3. Data Transformation
- Standardized features to ensure equal contribution to models.
- Split the dataset into **training (80%)** and **testing (20%)** sets for model evaluation.

---

## Feature Importance
- `Age` was the most important feature in predicting price.
- `Weight` and `MetColor` were also significant predictors.
- Features like `KM`, `HP`, `CC`, `Automatic`, and `Doors` were removed due to negligible importance.

---

