# linear-multiple-regression
# 🏡 Housing Price Prediction — Linear Regression

## 📌 Objective
This project predicts house prices using the Housing.csv dataset.  
The main goals are:
- Perform data preprocessing  
- Conduct exploratory data analysis  
- Build and evaluate a Linear Regression model  
- Interpret model results and coefficients  
- Remove one feature that did not improve the model
  
---

## 📂 Dataset Description
File used: **Housing.csv**

Contains the following types of features:

**Numerical Features**
- area  
- bedrooms  
- bathrooms  
- stories  
- parking  

**Binary (yes/no) Features**
- mainroad  
- guestroom  
- basement  
- hotwaterheating  
- airconditioning  
- prefarea  

**Categorical Feature**
- furnishingstatus (furnished / semi-furnished / unfurnished)

**Target Variable**
- price

---

## 🛠️ Tools Used
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  

---

## ✔️ Complete Workflow

### **1️⃣ Data Loading**
The dataset was imported, inspected for missing values, duplicates, and overall structure.

---

### **2️⃣ Data Preprocessing**
The following preprocessing steps were applied:

- Converted all **yes/no** features into numeric values  
- Converted **furnishingstatus** into multiple separate columns (one-hot encoding)  
- Removed duplicate rows to avoid data leakage  
- Checked for incorrect or inconsistent data  
- Prepared the final features and target variable  

---

### **3️⃣ Exploratory Data Analysis (EDA)**
Performed several EDA steps including:

- Understanding distributions of key variables  
- Checking relationships between features and price  
- Plotting a correlation heatmap using only numeric features  
- Identifying patterns such as which features most influence price  

---

### **4️⃣ Feature Removal**
One feature was removed from the dataset because:
- It did not improve model performance  
- It added unnecessary noise or redundancy  

Removing low-impact features helps the model generalize better.

---

## **5️⃣ Train–Test Split**
The cleaned dataset was split into:
- **80% training data**
- **20% testing data**

This separation ensures unbiased model evaluation.

---

## **6️⃣ Multiple Regression Model**
A **Multiple Linear Regression** model was built using all processed features except the removed one.

The model learned the relationship between each feature and house price.

---

## **7️⃣ Model Evaluation**
The following metrics were calculated:

- **MAE (Mean Absolute Error):** approximately 7.3 Lakhs  
- **MSE (Mean Squared Error):** large value due to squared magnitudes  
- **RMSE (Root Mean Squared Error):** approximately 9.7 Lakhs  
- **R² Score:** around 0.67  

### Why are the errors large?
Because house prices in the dataset are very high (lakhs to millions).  
Naturally, absolute and squared errors also become large.  
This is normal for a high-value regression problem.

---

## **8️⃣ Coefficient Interpretation**
The regression coefficients indicate:

- How strongly each feature affects the price  
- Which attributes increase price  
- Which ones decrease price  

Examples:
- Larger area increases price  
- Furnishing status influences price  
- Parking, air conditioning, and location features have positive impact  

---

## 📈 Final Insights
- The Linear Regression model performs reasonably well with **67% accuracy** (R² = 0.67)  
- It captures key trends but can be improved  
- Removing an unnecessary feature helped simplify the model  
- Serves as a solid baseline for future improvements

---

## 🚀 Future Improvements
- Apply log transformation to price  
- Remove outliers  
- Use Ridge and Lasso regression for penalty-based modeling  
- Test tree-based models such as Random Forest or XGBoost  
- Perform cross-validation  
