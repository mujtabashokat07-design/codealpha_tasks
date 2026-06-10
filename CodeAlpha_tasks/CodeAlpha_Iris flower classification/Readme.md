# CodeAlpha_Iris_flower_project

A professional end-to-end Machine Learning project that classifies Iris flower species (*Iris-setosa*, *Iris-versicolor*, *Iris-virginica*) based on their morphological measurements (sepal length, sepal width, petal length, and petal width). 

This repository contains a clean, reproducible implementation utilizing **Scikit-Learn** and **Pandas**.

---

## 📌 Project Overview
Classification is a fundamental concept in supervised machine learning. This project demonstrates how to ingest raw tabular data, preprocess it, split it for reliable evaluation, and train an ensemble model (**Random Forest Classifier**) to achieve high classification accuracy.

### Key Features:
- **Data Preprocessing**: Removal of redundant identifiers and automated feature-target separation.
- **Stratified Splitting**: Ensures balanced class distributions across training and testing sets to prevent evaluation bias.
- **Robust Modeling**: Utilizes a Random Forest ensemble to capture non-linear decision boundaries.
- **Detailed Evaluation**: Full breakdown of performance using Accuracy, Precision, Recall, F1-Score, and a Confusion Matrix.

---

## 📊 Dataset Description
The project uses the classic **Iris Dataset** (`Iris.csv`). The dataset contains 150 records with 6 columns:

| Column Name | Data Type | Description | Role |
| :--- | :--- | :--- | :--- |
| `Id` | Integer | Unique identifier for each row | Dropped (Not a feature) |
| `SepalLengthCm` | Float | Length of the flower's sepal (cm) | Continuous Feature |
| `SepalWidthCm` | Float | Width of the flower's sepal (cm) | Continuous Feature |
| `PetalLengthCm` | Float | Length of the flower's petal (cm) | Continuous Feature |
| `PetalWidthCm` | Float | Width of the flower's petal (cm) | Continuous Feature |
| `Species` | Object / String | The target class name (`Iris-setosa`, `Iris-versicolor`, `Iris-virginica`) | **Target Variable** |

---

## ⚙️ Installation & Setup

### 1. Clone the Repository
```bash
git clone [https://github.com/your-username/iris-classification.git](https://github.com/your-username/iris-classification.git)
cd iris-classification