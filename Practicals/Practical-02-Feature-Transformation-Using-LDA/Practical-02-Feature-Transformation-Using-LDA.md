# Practical 02: Feature Transformation Using LDA

## 📌 Aim

Apply the **Linear Discriminant Analysis (LDA)** algorithm for dimensionality reduction on the same high-dimensional dataset used in Practical 01 and compare its performance and computational efficiency with the **Principal Component Analysis (PCA)** algorithm.

---

## 🎯 Objectives

* Understand the concept of **Linear Discriminant Analysis (LDA)**.
* Perform dimensionality reduction using LDA.
* Compare LDA with PCA using the same dataset.
* Evaluate the effect of dimensionality reduction on model accuracy.
* Measure and compare the computational efficiency of both techniques.

---

## 🛠️ Tools & Libraries Used

* Python
* NumPy
* Pandas
* Scikit-learn
* Jupyter Notebook
* Time Module

---

## 📂 Dataset

**Digits Dataset** (from Scikit-learn)

* Total Samples: **1,797**
* Total Features: **64**
* Total Classes: **10 (Digits 0–9)**

The same dataset from Practical 01 is used to ensure a fair comparison between PCA and LDA.

---

## 📖 Concepts Covered

* Feature Transformation
* Dimensionality Reduction
* Principal Component Analysis (PCA)
* Linear Discriminant Analysis (LDA)
* Data Standardization
* Logistic Regression
* Model Performance Evaluation
* Computational Efficiency

---

## 🚀 Workflow

1. Import the required Python libraries.
2. Load the Digits dataset.
3. Standardize the feature values using `StandardScaler`.
4. Split the dataset into training and testing sets.
5. Apply **PCA** to reduce the feature dimensions.
6. Train a Logistic Regression model on the PCA-transformed data.
7. Apply **LDA** to reduce the feature dimensions using class labels.
8. Train another Logistic Regression model on the LDA-transformed data.
9. Compare both models based on:

   * Classification Accuracy
   * Execution Time

---

## 📊 Expected Outcome

* Successfully reduce the dimensionality of the Digits dataset using **LDA**.
* Compare the performance of **PCA** and **LDA** using the same Machine Learning model.
* Observe differences in classification accuracy and execution time.
* Understand that **PCA is an unsupervised dimensionality reduction technique**, while **LDA is a supervised dimensionality reduction technique** that uses class labels to maximize class separability.

---

## 📌 Conclusion

This practical demonstrates how **Linear Discriminant Analysis (LDA)** can be used for feature transformation and compares its performance with **Principal Component Analysis (PCA)**. By evaluating both methods on the same high-dimensional dataset using Logistic Regression, we gain a better understanding of their impact on model accuracy and computational efficiency.

---

## 👨‍💻 Author

**Om Dadaji Pawar**

---

## 🌐 Connect with Me

* **GitHub:** https://github.com/Om-Pawar-9834
* **LinkedIn:** https://www.linkedin.com/in/om-pawar-a5307b330/

