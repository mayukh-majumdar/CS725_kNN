# Generalization Study of kNN with Different Distance Metrics

This project investigates how various distance metrics affect the generalization performance of the **k-Nearest Neighbors (kNN)** classifier using the **Iris dataset**. The study evaluates multiple metrics across a range of k-values, computes test-set accuracy, performs cross-validation, generates confusion matrices, and saves all visualizations automatically.

---

## Overview

The performance of kNN is deeply influenced by the distance function used to measure similarity. This project provides a structured experimental setup to compare different metrics and observe how they shape the classifier’s behavior.

The metrics evaluated include:

- **Euclidean**
- **Manhattan**
- **Chebyshev**
- **Minkowski (p = 3, p = 4)**
- **Cosine**
- **Mahalanobis**

The notebook saves:

- Accuracy curves across all metrics
- Individual metric-wise curves
- Cross-validation accuracy plots
- Confusion matrices for best-performing k per metric

All plots are saved into the `Plots/` directory.

---

## Badges

![Python](https://img.shields.io/badge/Python-3.12%2B-blue.svg)
![Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3%2B-F7931E.svg)
![Dataset](https://img.shields.io/badge/Data-Iris-4CAF50.svg)
![Status](https://img.shields.io/badge/Project-Active-brightgreen.svg)
![License](https://img.shields.io/badge/License-MIT-darkgreen.svg)

---

## Working With the Code

Below are the essentials for navigating or extending the notebook.

### **1. Running the Notebook**

Open `knn_notebook.ipynb` in Jupyter Notebook or VS Code and run cells in order. Required folders (`data/`, `Plots/`) are created automatically.

### **2. Editing Distance Metrics**

To add or remove metrics, modify the dictionary:

```python
distance_metrics = {
    'euclidean': 'euclidean',
    'manhattan': 'manhattan',
    ...
}
```

If your metric needs parameters, follow the existing structured examples.

### **3. Modifying k-Range**

Update:

```python
k_values = range(1, 31)
```

to change the number of neighbors evaluated.

### **4. Cross-Validation Notes**

Cross-validation uses `Pipeline` to prevent data leakage. You can adjust fold count via:

```python
cross_val_score(pipe, X, y, cv=<folds>)
```

---

## Requirements

The project requires:

- Python 3.12+
- numpy
- pandas
- matplotlib
- scikit-learn
- jupyter

Install them using:

```bash
pip install -r requirements.txt
```

---

## Summary

This project offers a clean and reproducible framework to analyze how different distance metrics shape the generalization ability of kNN. It is designed to be easily extensible and suitable for experimentation, coursework or deeper exploration of metric-based learning.

---
