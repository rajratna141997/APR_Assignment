
# Classifying Forest fire size categories (Small, Large) using SVM

## Project Overview

This project applies Support Vector Machines (SVMs) to the Forest Fires dataset to classify the burned area size of a forest fire into two categories:

Small (low burned area)

Large (high burned area)

The motivation behind this work is to leverage machine learning techniques to assist in forest fire risk assessment, resource allocation, and disaster management.


## Dataset

The dataset used is forestfires.csv, originally from the UCI Machine Learning Repository.

#Features

Spatial Attributes: X, Y (location coordinates)

Temporal Attributes: month, day (time of occurrence)

Meteorological Variables: temp (temperature), RH (relative humidity), wind (wind speed), rain (rainfall)

Fire Weather Indices: FFMC, DMC, DC, ISI (standard measures used in forest fire danger rating systems)

Target Variable: area (burned area in hectares)

#Target Transformation

Since the raw area feature is continuous, it was converted into a binary categorical variable:

Small fire if area < threshold

Large fire if area ≥ threshold

This enables SVM classification into two distinct size categories.

---

## ⚙️ Methodology

The project followed a structured workflow:

1. **Data Preprocessing**

   * Encoded categorical variables into numerical form.
   * Scaled features using both *Min-Max Scaling* and *Standard Scaling*.
   * Visualized data distribution to understand class balance and feature correlations.

2. **Model Training with SVM**

   * Implemented **Support Vector Classifier (SVC)** from scikit-learn.
   * Explored different kernel functions such as **Linear Kernel** and **Radial Basis Function (RBF) Kernel**.
   * Experimented with parameters like **C** (regularization) and **gamma** (influence of single training examples) to optimize performance.

3. **Evaluation Metrics**

   * Accuracy score to measure overall correctness.
   * Confusion matrix to analyze misclassifications.
   * Classification report showing precision, recall, and F1-score.
   * Visualizations of decision boundaries to demonstrate how SVM separates classes.

---

## 📊 Results

The evaluation showed that:

* The **accuracy** of the SVM classifier was high, indicating that the model successfully classified most samples.
* The **confusion matrix** revealed that the majority of predictions were correct, though some misclassifications occurred between closely related classes.
* The **classification report** highlighted strong performance with balanced precision and recall across classes.
* Visualization of the **decision boundary** clearly illustrated how SVM separates classes in feature space.

These results demonstrate the strength of SVM in handling classification tasks with proper preprocessing.

---

## 🚀 Applications of SVM

Support Vector Machines are widely used in real-world applications, including:

* **Text Classification:** Spam filtering, sentiment analysis, document categorization.
* **Image Recognition:** Handwritten digit recognition, facial recognition, and object detection.
* **Bioinformatics:** Classification of diseases such as cancer based on gene expression data.
* **Financial Predictions:** Fraud detection, credit risk classification, and stock market trend analysis.

---

## ⚠️ Limitations

While SVMs are powerful, they come with certain limitations:

* **Scalability Issues:** Training SVMs on very large datasets is computationally expensive.
* **Kernel Selection:** Choosing the correct kernel function requires experimentation and domain knowledge.
* **Sensitivity to Parameters:** Performance depends heavily on hyperparameters like `C` and `gamma`.
* **Interpretability:** SVMs can be less interpretable compared to decision trees or rule-based models.

---

## ✅ Conclusion

This project successfully demonstrated the use of **Support Vector Machines** for classification tasks.
The experiments confirmed that SVMs are capable of achieving strong accuracy and robust classification performance when the dataset is properly preprocessed.

The project also highlighted the importance of feature scaling and parameter tuning in ensuring that SVM performs optimally.

For future improvements, additional techniques could be explored, such as:

* **Hyperparameter Optimization** using Grid Search or Bayesian Optimization.
* **Cross-validation** for more reliable model evaluation.
* **Kernel Tricks** for handling more complex datasets that are not linearly separable.

---

