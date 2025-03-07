# Logistic Regression: A Mathematical Approach
Repository aimed at explaining the mathematical concepts behind the logistic regression model.

<p align="center">
  <img src="https://github.com/VictorFrancheto/Mathematics_and_Machine_Learning/blob/main/machine.JPG">
</p>

# 📊 Logistic Regression: A Step-by-Step Guide

**Logistic Regression** is a fundamental algorithm for **binary classification**, widely used in machine learning and statistics. Despite its name, it is a **classification** algorithm, not a regression technique.

Let’s break it down step by step! 🚀

---

## 🔍 What is Logistic Regression?

Logistic Regression models the **probability** that a given input belongs to a particular class. Unlike linear regression, which predicts continuous values, logistic regression outputs probabilities and applies a threshold to classify observations.

Mathematically, given an input feature vector \( x \), the model computes:

$$ P(y=1 | x) = \sigma(w^T x + b), $$

where:\
✔ \( w \) = weight vector (learned parameters)\
✔ \( b \) = bias term\
✔ \( \sigma(z) \) = **sigmoid function**:

   $$ \sigma(z) = \frac{1}{1 + e^{-z}}. $$

This function maps any real-valued number into the range \( (0,1) \), making it ideal for probability estimation.

---

## ⚙️ How Does Logistic Regression Work?

1️⃣ **Compute the Linear Combination**:  
   Compute the weighted sum of input features:

   $$ z = w^T x + b. $$

2️⃣ **Apply the Sigmoid Function**:  
   Convert \( z \) into a probability:

   $$ P(y=1 | x) = \frac{1}{1 + e^{-z}}. $$

3️⃣ **Set a Decision Threshold**:  
   If the probability is above a certain threshold (typically **0.5**), classify as **positive (1)**, otherwise classify as **negative (0)**:

   $$ \hat{y} = \begin{cases} 1, & P(y=1 | x) \geq 0.5 \\ 0, & \text{otherwise} \end{cases} $$

---

## 🔢 Training Logistic Regression

The goal is to find the **best parameters** \( w \) and \( b \) that minimize classification errors. This is done using:

📌 **Loss Function (Log-Loss or Cross-Entropy)**:  

   $$ L = - \frac{1}{n} \sum_{i=1}^{n} \left[ y_i \log P(y_i | x_i) + (1 - y_i) \log (1 - P(y_i | x_i)) \right]. $$

📌 **Optimization (Gradient Descent)**:  
   The weights \( w \) are updated iteratively using:

   $$ w := w - \alpha \frac{\partial L}{\partial w}, $$

   where \( \alpha \) is the learning rate.

---

## 📏 Evaluating Performance

Logistic Regression is evaluated using several metrics:

✔ **Accuracy**: Measures overall correctness.
✔ **Precision & Recall**: Handle imbalanced datasets.
✔ **F1-Score**: Harmonic mean of precision and recall.
✔ **ROC Curve & AUC**: Assess probability calibration.

---

## ⚠️ Key Considerations

📌 **Feature Scaling**: Since weights are optimized via gradient descent, it’s essential to normalize features.
📌 **Overfitting**: Regularization techniques like **L2 (Ridge Regression)** prevent overfitting.
📌 **Linearity Assumption**: Logistic Regression assumes a **linear relationship** between input features and log-odds.


  
