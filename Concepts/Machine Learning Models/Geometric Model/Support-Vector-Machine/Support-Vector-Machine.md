# Geometric Model using Support Vector Machine (SVM)

## 📖 Overview

This practical demonstrates the **Geometric Model** in Machine Learning using the **Support Vector Machine (SVM)** algorithm.

A **Geometric Model** represents every data sample as a **point in a feature space**. Instead of using logical rules or probability distributions, it learns by analyzing the **geometric relationship** between data points.

Unlike K-Nearest Neighbors (KNN), which classifies data based on the nearest neighbors, **Support Vector Machine (SVM)** classifies data by finding the **best decision boundary (hyperplane)** that separates different classes.

---

# 🎯 Objective

The objective of this practical is to:

* Understand the concept of a Geometric Model.
* Learn how the Support Vector Machine (SVM) algorithm works.
* Understand the concepts of **hyperplane**, **margin**, and **support vectors**.
* Classify data using the optimal decision boundary.
* Predict the class of a new data sample.

---

# 📐 What is a Geometric Model?

A **Geometric Model** is a machine learning approach in which every data sample is represented as a **point in a feature space**.

Each feature becomes one dimension.

For example, if we use two features:

* Weight
* Sweetness

then every fruit becomes a point.

| Fruit  | Weight | Sweetness | Point   |
| ------ | ------ | --------- | ------- |
| Apple  | 150    | 8         | (150,8) |
| Apple  | 160    | 7         | (160,7) |
| Apple  | 170    | 8         | (170,8) |
| Orange | 120    | 5         | (120,5) |
| Orange | 130    | 4         | (130,4) |
| Orange | 140    | 5         | (140,5) |

The model studies the position of these points and finds the best way to separate different classes.

---

# 🤔 Why is SVM a Geometric Model?

SVM is called a **Geometric Model** because it uses geometric concepts such as:

* Points
* Vectors
* Distance
* Decision Boundary
* Hyperplane
* Margin

Instead of asking,

> **"Which points are nearest?"**

like KNN,

SVM asks,

> **"What is the best boundary that separates different classes?"**

Since it uses geometry to solve classification problems, SVM belongs to the **Geometric Model** category.

---

# 📚 Why Do We Use SVM?

Support Vector Machine is widely used because:

* It provides high classification accuracy.
* It finds the optimal boundary between classes.
* It works well even when there are many features.
* It reduces classification errors by maximizing the margin.
* It performs well on both small and medium-sized datasets.

---

# ⚙️ Working of SVM

The SVM algorithm follows these steps.

---

## Step 1: Collect Training Data

Provide the training dataset along with labels.

Example:

| Weight | Sweetness | Fruit  |
| ------ | --------- | ------ |
| 150    | 8         | Apple  |
| 160    | 7         | Apple  |
| 170    | 8         | Apple  |
| 120    | 5         | Orange |
| 130    | 4         | Orange |
| 140    | 5         | Orange |

---

## Step 2: Represent Data as Points

Each fruit becomes a point.

Example:

* Apple → (150,8)
* Apple → (160,7)
* Orange → (120,5)
* Orange → (130,4)

Now all data points are placed in the feature space.

---

## Step 3: Find the Best Decision Boundary

Many lines can separate Apples and Oranges.

However, SVM does **not** choose just any line.

It finds the line that creates the **largest possible distance** between the two classes.

This line is called the **Decision Boundary** or **Hyperplane**.

Example:

```text
Sweetness ↑

8 |                🍎
  |         🍎
7 |               🍎

===========================  Hyperplane

5 | 🍊         🍊

4 |      🍊

----------------------------------------→ Weight
```

---

## Step 4: Identify Support Vectors

The data points closest to the decision boundary are called **Support Vectors**.

These points determine where the hyperplane should be placed.

Example:

```text
🍎      ⭐

======================

⭐      🍊
```

The ⭐ points are the **Support Vectors**.

If these points move, the decision boundary also changes.

---

## Step 5: Maximize the Margin

The distance between the decision boundary and the nearest support vectors is called the **Margin**.

SVM always tries to maximize this margin.

A larger margin generally leads to better classification of new data.

---

## Step 6: Train the Model

```python
model.fit(X, y)
```

During training, SVM learns the optimal decision boundary.

Unlike KNN, SVM does not simply store all training data. It learns a boundary that separates the classes.

---

## Step 7: New Data Arrives

Suppose a new fruit has:

* Weight = 155 grams
* Sweetness = 8

The model places this fruit in the feature space.

---

## Step 8: Predict

The model checks:

> **On which side of the decision boundary does the new fruit lie?**

If it lies on the Apple side,

Prediction = **Apple**

If it lies on the Orange side,

Prediction = **Orange**

---

# 🖼 Simple Visualization

```text
Sweetness ↑

9 |

8 |                 🍎
  |         🍎      ⭐ New Fruit
7 |               🍎

============================

5 | 🍊         🍊

4 |      🍊

--------------------------------------→ Weight
```

Since the new fruit lies on the Apple side of the decision boundary,

Prediction = **Apple**

---

# 💻 Python Implementation

The notebook included in this folder implements SVM using the following steps:

1. Import `SVC` from Scikit-learn.
2. Create the training dataset.
3. Create labels.
4. Train the SVM model.
5. Predict the class of a new fruit.
6. Display the prediction.

---

# 🌍 Real-World Applications

Support Vector Machine is widely used in:

* Face Recognition
* Image Classification
* Handwriting Recognition
* Spam Email Detection
* Medical Diagnosis
* Text Classification
* Bioinformatics

---

# ✅ Advantages

* High classification accuracy.
* Finds the optimal decision boundary.
* Effective for high-dimensional data.
* Good generalization to unseen data.
* Less prone to overfitting due to margin maximization.

---

# ❌ Limitations

* Training can be slow for very large datasets.
* Selecting the correct kernel may require experimentation.
* More difficult to understand than KNN.
* Sensitive to noisy or overlapping data.

---

# 📊 SVM as a Geometric Model

| Property              | Description                                                         |
| --------------------- | ------------------------------------------------------------------- |
| Machine Learning Type | Supervised Learning                                                 |
| Model Category        | Geometric Model                                                     |
| Learning Method       | Uses labeled training data                                          |
| Main Concept          | Hyperplane and Maximum Margin                                       |
| Prediction Method     | Determines on which side of the decision boundary the new data lies |

---

# 🔄 Difference Between KNN and SVM

| Feature         | KNN                     | SVM                    |
| --------------- | ----------------------- | ---------------------- |
| Learning Type   | Supervised              | Supervised             |
| Model Category  | Geometric Model         | Geometric Model        |
| Main Concept    | Distance between points | Best decision boundary |
| Prediction      | Nearest neighbors       | Hyperplane             |
| Decision Method | Majority Voting         | Margin Maximization    |

---

# 🎓 Learning Outcome

After completing this practical, you will be able to:

* Understand the concept of a Geometric Model.
* Explain why SVM is a Geometric Model.
* Understand hyperplanes, margins, and support vectors.
* Classify data using the optimal decision boundary.
* Differentiate between KNN and SVM.
* Apply SVM to solve classification problems.

---

# 🎯 Conclusion

The **Support Vector Machine (SVM)** algorithm is one of the most powerful **Geometric Models** in Machine Learning. It represents data as points in a feature space and classifies them by finding the **optimal decision boundary (hyperplane)** with the **maximum possible margin** between different classes.

Unlike KNN, which predicts based on the nearest neighbors, SVM learns the best boundary during training and uses that boundary to classify new data. This makes SVM highly effective for many real-world classification problems such as face recognition, spam detection, image classification, handwriting recognition, and medical diagnosis.
