# Practical 01: Feature Transformation Using PCA

## 📌 Aim

Apply the **Principal Component Analysis (PCA)** algorithm for dimensionality reduction on a high-dimensional dataset and observe the influence of feature reduction on model performance and computational efficiency.

---

## 🎯 Objectives

* Understand the concept of **Principal Component Analysis (PCA)**.
* Reduce the dimensionality of a high-dimensional dataset while preserving most of its information.
* Compare the performance of a Machine Learning model before and after applying PCA.
* Analyze the impact of feature reduction on training time, prediction time, and classification accuracy.

---

## 🛠️ Tools & Libraries Used

* Python
* Pandas
* Scikit-learn
* Jupyter Notebook
* Time Module

---

## 📂 Dataset

**Breast Cancer Wisconsin Dataset** (from Scikit-learn)

* Total Samples: **569**
* Total Features: **30**
* Target Classes: **2**

  * Malignant
  * Benign

---

## 📖 Concepts Covered

* Feature Transformation
* Dimensionality Reduction
* Principal Component Analysis (PCA)
* Data Standardization
* Random Forest Classifier
* Model Performance Evaluation
* Computational Efficiency

---

## 🚀 Workflow

1. Import the required Python libraries.
2. Load the Breast Cancer Wisconsin dataset.
3. Split the dataset into training and testing sets.
4. Standardize the feature values using `StandardScaler`.
5. Train a **Random Forest Classifier** without applying PCA.
6. Record:

   * Number of features
   * Training time
   * Prediction time
   * Classification accuracy
7. Apply **PCA** while retaining **95% of the variance**.
8. Train the Random Forest Classifier using the PCA-transformed data.
9. Compare the results before and after applying PCA.

---

## 📊 Performance Comparison

The practical compares the following metrics:

* Number of Features
* Training Time
* Prediction Time
* Classification Accuracy

The comparison helps evaluate how dimensionality reduction affects both model performance and computational efficiency.

---

## 📌 Expected Outcome

* Successfully reduce the number of features using **Principal Component Analysis (PCA)**.
* Preserve most of the important information while reducing dimensionality.
* Observe the impact of PCA on training speed, prediction speed, and model accuracy.
* Understand how PCA helps simplify high-dimensional datasets while maintaining good predictive performance.

---

## 📌 Conclusion

This practical demonstrates the application of **Principal Component Analysis (PCA)** for feature transformation. By comparing the Random Forest model before and after dimensionality reduction, it becomes easier to understand how PCA improves computational efficiency while retaining most of the important information required for accurate classification.

---

## 👨‍💻 Author

**Om Dadaji Pawar**

---

## 🌐 Connect with Me

* **GitHub:** https://github.com/Om-Pawar-9834
* **LinkedIn:** https://www.linkedin.com/in/om-pawar-a5307b330/
