# privacy_ml

### Overview

This project explores several privacy and machine learning concepts through empirical experiments implemented in Python. The repository investigates information leakage in machine learning models and evaluates differentially private mechanisms for statistical queries and regression.

The experiments are organized into three main parts: label recovery from random projections, model inversion attacks on logistic regression, and differentially private data analysis.

### Part 1 — Label Recovery and Model Inversion

The first part studies the recovery of binary labels from random projections. Labels are observed through dot products with random sign matrices, and reconstruction is performed using least squares estimation via the pseudo-inverse. Performance is evaluated using ROC and DET curves while analyzing how the number of projections affects recovery.

The analysis also examines how partial knowledge of labels improves reconstruction accuracy.

A logistic regression model is then trained on the dataset to study privacy risks. Two attacks are implemented:

* **Gradient-based model inversion**, which exploits gradients of the logistic loss to infer unknown labels.
* **Nearest-neighbor reconstruction**, which estimates labels by comparing predicted probabilities with those of known samples.

### Part 2 — Differential Privacy Mechanisms

The second part implements several classical differential privacy mechanisms.

Experiments include:

* **Laplace mechanism for counting queries**
* **Differentially private maximum estimation**
* **Noisy argmax using Laplace noise**
* **Argmax using the exponential mechanism**

The experiments illustrate the privacy–accuracy tradeoff by analyzing the impact of different privacy budgets ( \epsilon ).

### Part 3 — Differentially Private Linear Regression

The final section studies linear regression under differential privacy.

The following approaches are implemented and compared:

* **Ordinary Least Squares (OLS)**
* **Gaussian-perturbed OLS**
* **Gradient Descent**
* **Differentially Private Gradient Descent (DP-GD)**
* **Clipped DP-GD with adaptive step sizes**

The analysis evaluates the accuracy of private models using RMSE and examines how performance varies with the privacy parameter.

### Technologies

* Python
* NumPy
* scikit-learn
* Pandas
* Matplotlib

### Goal

The project provides practical demonstrations of privacy risks in machine learning models and evaluates standard differential privacy mechanisms in statistical learning tasks.
