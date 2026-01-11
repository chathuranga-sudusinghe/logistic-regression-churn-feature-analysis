# Logistic Regression Churn Feature Analysis

## 📌 Project Overview
This project explores **Logistic Regression** for customer churn prediction using a
telecommunications dataset. The objective is not only to build a predictive model,
but also to deeply understand **model optimization**, **cost functions**, and
**feature impact on probabilistic performance**.

The project combines:
- Mathematical foundations
- From-scratch implementation
- Visual intuition
- Scikit-learn comparison
- Feature impact experimentation

---

## 🎯 Objectives
- Understand Logistic Regression from a theoretical perspective
- Implement Logistic Regression **from scratch** using Gradient Descent
- Visualize the **log loss cost function** in 2D and 3D
- Compare **Batch Gradient Descent** and **Stochastic Gradient Descent**
- Train and evaluate a Logistic Regression model using **Scikit-learn**
- Analyze how **feature selection** affects model performance using log loss

---

## 📊 Dataset
The dataset represents customer demographic and service-related information from
a hypothetical telecommunications company.

### Target Variable
- **churn**  
  - `1` → Customer left the company  
  - `0` → Customer stayed with the company  

### Features Used
- `tenure`: Years the customer has been with the company  
- `age`: Customer age  
- `address`: Years at current address  
- `income`: Approximate annual income  
- `ed`: Education level (ordinal)  
- `employ`: Years employed  
- `equip`: Equipment ownership indicator  

---

## 🧠 Methodology

### 1. Logistic Regression from Scratch
- Implemented sigmoid function
- Implemented log loss cost function
- Implemented Batch Gradient Descent
- Tracked cost reduction over iterations

### 2. Optimization Visualization
- 2D plot of cost vs iterations
- 3D visualization of log loss surface
- Overlay of Gradient Descent optimization path

### 3. Optimization Strategies
- Batch Gradient Descent (BGD)
- Stochastic Gradient Descent (SGD)
- Visual comparison of convergence behavior

### 4. Scikit-learn Implementation
- Trained Logistic Regression using Scikit-learn
- Predicted probabilities
- Evaluated performance using **log loss**

### 5. Feature Impact Analysis
- Baseline model using all features
- Experiments removing individual features
- Performance comparison using log loss

---

## 📈 Results Summary

| Experiment | Log Loss |
|----------|----------|
| Baseline | 0.4069 |
| Remove equip | 0.4485 |
| Remove income | 0.4050 |
| Remove employ | **0.3888** |
| Remove income & employ | 0.3933 |

**Key Insight:**  
Removing the `employ` feature resulted in the best performance, indicating that
feature redundancy can negatively impact probabilistic predictions.

---

## 🔍 Key Learnings
- Logistic Regression optimizes a **convex log loss function**, guaranteeing a
  single global minimum.
- Gradient Descent behavior can be clearly understood through cost surface
  visualization.
- Feature quantity does not guarantee better performance — **feature quality
  matters more**.
- Removing redundant or weak features can improve probability calibration.

---

## 🛠️ Tools & Technologies
- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## 📂 Repository Structure
