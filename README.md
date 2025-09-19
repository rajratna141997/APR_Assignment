
# Classifying Forest fire size categories (Small, Large) using SVM

## Project Overview

This project applies Support Vector Machines (SVMs) to the Forest Fires dataset to classify the burned area size of a forest fire into two categories:

* Small (low burned area)

* Large (high burned area)

The motivation behind this work is to leverage machine learning techniques to assist in forest fire risk assessment, resource allocation, and disaster management.


## Dataset

The dataset used is forestfires.csv, originally from the UCI Machine Learning Repository.

# Features

Spatial Attributes: X, Y (location coordinates)

Temporal Attributes: month, day (time of occurrence)

Meteorological Variables: temp (temperature), RH (relative humidity), wind (wind speed), rain (rainfall)

Fire Weather Indices: FFMC, DMC, DC, ISI (standard measures used in forest fire danger rating systems)

Target Variable: area (burned area in hectares)

# Target Transformation

Since the raw area feature is continuous, it was converted into a binary categorical variable:

* Small fire if area < threshold

* Large fire if area ≥ threshold

This enables SVM classification into two distinct size categories.

---

## Methodology

The project followed a structured workflow:

1. **Data Preprocessing**

  * Encoding: Converted categorical features (month, day) into numerical form using label encoding.

  * Feature Scaling:

    * Min-Max Scaling to normalize feature values between 0 and 1.

    * Standard Scaling to standardize features for SVM kernels.

  * Data Splitting: Divided dataset into 70% training and 30% testing.

2. **Model Training with SVM**

* Support Vector Classifier (SVC) was implemented.

* Kernels tested:

  Linear Kernel: For linearly separable data.

  RBF Kernel: To handle non-linear decision boundaries.

* Hyperparameters tuned:

* C (Regularization parameter): Controlled trade-off between margin size and misclassification.

* Gamma: Controlled influence of individual points on the decision boundary.

3. **Evaluation Metrics**

* Accuracy Score: Overall classification accuracy.

* Confusion Matrix: Breakdown of true/false positives and negatives.

* Classification Report: Precision, recall, F1-score.

* Visualizations: Plots of decision regions and accuracy performance.
---

## Results

The evaluation showed that:

* The **accuracy** of the SVM classifier was high, indicating that the model successfully classified most samples.
* The **confusion matrix** revealed that the majority of predictions were correct, though some misclassifications occurred between closely related classes.
* The **classification report** highlighted strong performance with balanced precision and recall across classes.
* Visualization of the **decision boundary** clearly illustrated how SVM separates classes in feature space.

---
