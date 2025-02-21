# 💎 Diamonds Price Prediction

## 📌 Overview
This project builds a **machine learning model** to predict diamond prices using **Ridge Regression**. The dataset includes features such as **carat, cut, color, clarity, depth, table, and volume**, which are preprocessed and engineered to improve model accuracy. Regularization is applied to prevent overfitting due to multicollinearity.

---

## 📊 Data Preprocessing
1. **Data Cleaning**  
   - Removed unnecessary columns (`Unnamed: 0`).  
   - Checked for missing values (none found).  
   - Identified and analyzed outliers but retained them since they impact pricing.

2. **Feature Engineering**  
   - Created a new feature **`volume`** by multiplying `x`, `y`, and `z`.  
   - Applied **log transformation** to `price` to normalize its distribution.  
   - Removed `x`, `y`, `z`, and `price` after deriving `volume`.

3. **Encoding Categorical Variables**  
   - Converted `cut`, `color`, and `clarity` into numerical values using Label Encoding.

4. **Handling Outliers**  
   - Used **quantile clipping** to cap extreme values in `volume` to avoid numerical instability.

---

## 🚀 Model Implementation
1. **Data Splitting & Scaling**  
   - Split the dataset into **training (80%)** and **testing (20%)** sets.  
   - Applied **StandardScaler** to normalize feature values.  

2. **Training Ridge Regression**  
   - Used **Ridge Regression** to handle multicollinearity.  
   - Applied **L2 regularization** to prevent overfitting.

3. **Model Evaluation**  
   - Measured performance using:  
     - **Mean Absolute Error (MAE)** – Measures average error.  
     - **Mean Squared Error (MSE)** – Penalizes large errors more.  
     - **R² Score** – Represents how well the model explains price variations.

---

## 📈 Results
| Metric | Value |
|--------|-------|
| **MAE** | `0.1584` |
| **MSE** | `0.0442` |
| **R² Score** | `0.9571` |
