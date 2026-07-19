# Geometric Model using K-Nearest Neighbors (KNN)

## 📖 Overview

This practical demonstrates the **Geometric Model** in Machine Learning using the **K-Nearest Neighbors (KNN)** algorithm.

A Geometric Model represents each data sample as a **point in a feature space**. Instead of using logical rules or probability, it learns patterns by measuring the **distance** between data points.

KNN is one of the simplest and most intuitive algorithms based on this concept, making it an excellent choice for understanding how geometric models work.

---

# 🎯 Objective

The objective of this practical is to:

* Understand the concept of a Geometric Model.
* Learn how KNN works.
* Classify data using the distance between data points.
* Predict the class of a new data sample using nearest neighbors.

---

# 📐 What is a Geometric Model?

A **Geometric Model** is a machine learning approach in which every data sample is represented as a **point in a geometric space (feature space)**.

Each feature of the data becomes one dimension.

For example, if we have two features:

* Weight
* Sweetness

then every fruit can be represented as a point:

| Fruit  | Weight | Sweetness | Point   |
| ------ | ------ | --------- | ------- |
| Apple  | 150    | 8         | (150,8) |
| Apple  | 160    | 7         | (160,7) |
| Orange | 120    | 5         | (120,5) |
| Orange | 130    | 4         | (130,4) |

The model studies the geometric relationship between these points to make predictions.

---

# 🤔 Why is KNN a Geometric Model?

KNN is called a **Geometric Model** because it uses **distance** between points to classify new data.

It does not use:

* Probability
* IF-ELSE rules
* Mathematical prediction equations

Instead, it simply asks:

> **"Which existing data points are closest to the new data point?"**

Since distance is a geometric concept, KNN belongs to the Geometric Model category.

---

# 📚 Why Do We Use KNN?

KNN is widely used because:

* It is easy to understand.
* It is simple to implement.
* It works well for small and medium-sized datasets.
* It does not require building a complex mathematical model.
* It predicts based on similarity between data samples.

---

# ⚙️ Working of KNN

The KNN algorithm follows these steps:

### Step 1: Collect Training Data

Provide examples with their correct labels.

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

### Step 2: Represent Data as Points

Each fruit is represented as a coordinate.

Example:

* Apple → (150, 8)
* Apple → (160, 7)
* Orange → (120, 5)

Now the dataset becomes a collection of points in a feature space.

---

### Step 3: Create the KNN Model

```python
model = KNeighborsClassifier(n_neighbors=3)
```

Here,

```text
n_neighbors = 3
```

means the algorithm will consider the **3 nearest neighbors** before making a prediction.

---

### Step 4: Train the Model

```python
model.fit(X, y)
```

Unlike many machine learning algorithms, KNN does **not** create a mathematical equation.

Instead, it simply stores the training data.

---

### Step 5: New Data Arrives

Suppose a new fruit has:

* Weight = 155 grams
* Sweetness = 8

The model represents it as:

```text
(155, 8)
```

---

### Step 6: Measure Distance

The algorithm calculates the distance between the new fruit and every fruit in the training dataset.

Example:

| Fruit          | Distance   |
| -------------- | ---------- |
| Apple (150,8)  | Very Close |
| Apple (160,7)  | Close      |
| Apple (170,8)  | Close      |
| Orange (120,5) | Far        |
| Orange (130,4) | Far        |
| Orange (140,5) | Far        |

---

### Step 7: Find the Nearest Neighbors

Since:

```text
K = 3
```

the algorithm selects the three closest fruits.

Nearest neighbors:

* Apple
* Apple
* Apple

---

### Step 8: Majority Voting

The algorithm counts the labels.

| Fruit  | Count |
| ------ | ----: |
| Apple  |     3 |
| Orange |     0 |

The class with the highest count is selected.

**Prediction: Apple**

---

# 🖼 Simple Visualization

```text
Sweetness ↑

9 |

8 |                 🍎
  |         🍎     ⭐ New Fruit
7 |               🍎

6 |

5 | 🍊         🍊

4 |      🍊

--------------------------------------→ Weight
```

The new fruit is closer to the Apple points.

Therefore, it is classified as **Apple**.

---

# 💻 Python Implementation

The notebook included in this folder implements KNN using the following steps:

1. Import `KNeighborsClassifier` from Scikit-learn.
2. Create the training dataset.
3. Create labels.
4. Train the KNN model.
5. Predict the class of a new fruit.
6. Display the prediction.

---

# 🌍 Real-World Applications

KNN is widely used in:

* Fruit Classification
* Image Recognition
* Face Recognition
* Handwriting Recognition
* Medical Diagnosis
* Recommendation Systems
* Pattern Recognition

---

# ✅ Advantages

* Easy to understand.
* Easy to implement.
* No complex mathematical model required.
* Good for classification tasks.
* Works well on small datasets.

---

# ❌ Limitations

* Prediction becomes slower as the dataset grows.
* Requires storing all training data.
* Sensitive to irrelevant or noisy features.
* Choosing the correct value of **K** is important.

---

# 📊 KNN as a Geometric Model

| Property              | Description                             |
| --------------------- | --------------------------------------- |
| Machine Learning Type | Supervised Learning                     |
| Model Category        | Geometric Model                         |
| Learning Method       | Uses labeled training data              |
| Main Concept          | Distance between data points            |
| Prediction Method     | Majority voting among nearest neighbors |

---

# 🎓 Learning Outcome

After completing this practical, you will be able to:

* Understand the concept of a Geometric Model.
* Explain why KNN is a Geometric Model.
* Represent data in a feature space.
* Understand how KNN measures distance.
* Predict new data using nearest neighbors.
* Differentiate KNN from other machine learning algorithms.

---

# 🎯 Conclusion

The **K-Nearest Neighbors (KNN)** algorithm is one of the simplest examples of a **Geometric Model** in Machine Learning. It represents every data sample as a point in a feature space and classifies new data by measuring the distance to existing data points.

Rather than relying on probability or logical rules, KNN uses the geometric relationship between points. It finds the nearest neighbors, performs majority voting, and predicts the class of the new data sample. This simple yet effective approach makes KNN an excellent algorithm for learning the fundamentals of geometric models.
