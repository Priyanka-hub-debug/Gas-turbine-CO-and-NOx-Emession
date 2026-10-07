# 🔥 CO Emission Prediction using Machine Learning

## 📌 Project Overview

This project focuses on predicting **Carbon Monoxide (CO) emissions** using Machine Learning regression algorithms.

The project uses environmental and gas turbine-related parameters such as **Ambient Temperature (AT), Ambient Pressure (AP), Ambient Humidity (AH), Air Filter Difference Pressure (AFDP), Gas Turbine Exhaust Pressure (GTEP), Turbine Inlet Temperature (TIT), Turbine After Temperature (TAT), Turbine Energy Yield (TEY), Compressor Discharge Pressure (CDP), and Nitrogen Oxides (NOX)** to predict CO emissions.

The project includes **data exploration, data cleaning, outlier handling, correlation analysis, feature selection, transformation, scaling, train-test splitting, model training, prediction, and model evaluation**.

Four Machine Learning regression algorithms were implemented and compared to identify the best-performing model.

---

## 🎯 Objectives

* Analyze the dataset and understand the relationship between different features.
* Perform data exploration and preprocessing.
* Check and handle missing values.
* Detect and handle outliers using the IQR method.
* Analyze correlations between features.
* Select the most relevant features using SelectKBest.
* Apply Power Transformation using Yeo-Johnson.
* Standardize the features using StandardScaler.
* Split the dataset into training and testing sets.
* Train multiple Machine Learning regression algorithms.
* Evaluate model performance using MAE, MSE, and R² Score.
* Compare the models and identify the best-performing algorithm.

---

## 🛠️ Technologies Used

* **Python**
* **Jupyter Notebook**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**

---

## 📊 Dataset

The dataset contains **7,411 records and 11 columns**.

The features include:

| Feature | Description                       |
| ------- | --------------------------------- |
| `AT`    | Ambient Temperature               |
| `AP`    | Ambient Pressure                  |
| `AH`    | Ambient Humidity                  |
| `AFDP`  | Air Filter Difference Pressure    |
| `GTEP`  | Gas Turbine Exhaust Pressure      |
| `TIT`   | Turbine Inlet Temperature         |
| `TAT`   | Turbine After Temperature         |
| `TEY`   | Turbine Energy Yield              |
| `CDP`   | Compressor Discharge Pressure     |
| `CO`    | Carbon Monoxide – Target Variable |
| `NOX`   | Nitrogen Oxides                   |

The target variable for prediction is **CO**.

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Exploration
   ↓
Data Cleaning
   ↓
Missing Value Check
   ↓
Correlation Analysis
   ↓
Outlier Handling using IQR
   ↓
Feature Selection using SelectKBest
   ↓
Yeo-Johnson Transformation
   ↓
Standard Scaling
   ↓
Train-Test Split
   ↓
Model Training
   ↓
Prediction
   ↓
Model Evaluation
   ↓
Model Comparison
   ↓
Best Model Selection
```

---

## 🧹 Data Preprocessing

### 1. Data Loading

The dataset was loaded using Pandas and inspected to understand its structure, features, data types, and statistical properties.

### 2. Missing Value Check

Missing values were checked using Pandas functions.

The dataset contained **no missing values**.

### 3. Duplicate Check

Duplicate records were checked during data preprocessing.

### 4. Exploratory Data Analysis

Exploratory Data Analysis was performed using:

* Descriptive statistics
* Correlation analysis
* Correlation heatmap
* Box plots
* Feature distribution analysis

### 5. Outlier Handling

Outliers were detected and handled using the **Interquartile Range (IQR)** method.

The IQR method uses:

```text
IQR = Q3 - Q1

Lower Bound = Q1 - 1.5 × IQR

Upper Bound = Q3 + 1.5 × IQR
```

Values outside the calculated limits were handled during preprocessing.

---

## 🎯 Feature Selection

**SelectKBest** with `f_regression` was used to identify the most relevant features for predicting CO.

The feature scores showed that the important features included:

* TIT
* TEY
* GTEP
* CDP
* AFDP
* NOX
* TAT
* AH
* AT
* AP

The selected features were then used for model training.

---

## 🔄 Data Transformation

A **Yeo-Johnson Power Transformation** was applied to the selected numerical features.

This transformation helps improve the distribution of the data before applying Machine Learning algorithms.

---

## 📏 Feature Scaling

**StandardScaler** was used to standardize the selected features.

The scaling step ensures that the input features are represented on a comparable scale before model training.

---

## ✂️ Train-Test Split

The processed dataset was divided into training and testing datasets using an **80:20 split**.

```text
Training Samples: 5,928
Testing Samples: 1,483
```

The split was performed using `random_state=40`.

---

## 🤖 Machine Learning Algorithms

Four regression algorithms were used in the project:

### 1. Linear Regression

Linear Regression was used as a baseline regression algorithm to predict CO emissions based on the selected input features.

### 2. Decision Tree Regressor

Decision Tree Regressor uses a tree-based structure to learn relationships between the input features and the target variable.

### 3. Random Forest Regressor

Random Forest Regressor is an ensemble Machine Learning algorithm that combines multiple decision trees to improve prediction performance.

### 4. Gradient Boosting Regressor

Gradient Boosting Regressor builds models sequentially, where each new model attempts to improve the errors made by previous models.

---

## 📊 Model Evaluation

The regression models were evaluated using three important metrics:

### MAE – Mean Absolute Error

Measures the average absolute difference between the actual and predicted values.

**Lower MAE indicates better performance.**

### MSE – Mean Squared Error

Measures the average squared difference between actual and predicted values.

**Lower MSE indicates better performance.**

### R² Score

Measures how well the model explains the variation in the target variable.

**Higher R² indicates better performance.**

---

## 📈 Model Comparison

| Model             |      MAE |      MSE | R² Score |
| ----------------- | -------: | -------: | -------: |
| Linear Regression |     0.35 |     0.23 |     0.70 |
| Decision Tree     |     0.31 |     0.24 |     0.69 |
| **Random Forest** | **0.23** | **0.13** | **0.83** |
| Gradient Boosting |     0.29 |     0.17 |     0.77 |

---

## 🏆 Best Performing Model

Based on the evaluation results, the **Random Forest Regressor** achieved the best overall performance.

**MAE:** 0.23

**MSE:** 0.13

**R² Score:** 0.83

Random Forest achieved the **highest R² score** and the **lowest MAE and MSE** among the four selected algorithms.

Therefore, **Random Forest Regressor** was the best-performing model for predicting CO emissions in this project.

---

## 📚 Key Learning Outcomes

Through this project, I gained practical knowledge of:

* Python for Machine Learning
* Data preprocessing
* Exploratory Data Analysis
* Correlation analysis
* Outlier handling
* Feature selection
* SelectKBest
* Yeo-Johnson transformation
* Feature scaling
* Train-Test Split
* Regression algorithms
* Model training and prediction
* MAE, MSE and R² evaluation
* Model comparison
* Selecting the best-performing model

---
## ⭐ Conclusion

This project demonstrates an end-to-end **Machine Learning regression workflow for predicting Carbon Monoxide (CO) emissions**.

The project covers data exploration, preprocessing, outlier handling, feature selection, Yeo-Johnson transformation, feature scaling, model training, and model evaluation.

Four regression algorithms were compared using **MAE, MSE, and R² Score**.

Among the four models, **Random Forest Regressor achieved the best performance with an R² Score of 0.83**, making it the best-performing model for CO prediction in this project.

---


