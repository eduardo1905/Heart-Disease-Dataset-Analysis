# Unsupervised Patient Risk Analysis: Heart Disease Clustering

## Project Overview
This project explores the application of **Unsupervised Machine Learning** to detect latent patterns in patient health data. 

Unlike traditional classification tasks that rely on pre-labeled diagnoses, this analysis utilizes **K-Means Clustering** to autonomously segment a patient population based on biometric markers (e.g., Cholesterol, BMI, Blood Pressure). The goal was to determine if the algorithm could reconstruct high-risk vs. low-risk profiles without access to ground-truth labels.

## Technologies Used
* **Language:** Python 3.x
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-learn (K-Means, StandardScaler)
* **Visualization:** Matplotlib, Seaborn

## Key Methodologies

### 1. Data Cleaning & Preprocessing
* Handled missing values to prevent skewing of distance calculations.
* **Feature Scaling:** Applied Standardization (Z-score normalization) to ensure all biometric features contributed equally to the Euclidean distance metric used by K-Means.

### 2. Exploratory Data Analysis (EDA)
* Visualized distributions of key health metrics to identify outliers.
* Analyzed correlations between variables (e.g., Age vs. Cholesterol) to understand potential risk factors before modeling.

### 3. K-Means Clustering
* Implemented K-Means clustering with **k=2** (representing "At Risk" and "Healthy" segments).
* **Centroid Analysis:** Interpreted the resulting clusters by examining the mean values of features within each group.

## Results & Insights
The model successfully converged into two distinct patient clusters. By analyzing the cluster centroids, we observed clear distinctions:

* **Cluster 0 (Potential High Risk):** Characterized by higher average [Metric 1, e.g., Cholesterol] and [Metric 2, e.g., Age].
* **Cluster 1 (Potential Low Risk):** Characterized by lower average values across cardiac risk factors.

This suggests that unsupervised learning can effectively identify risk stratification patterns in health data even in the absence of diagnostic labels.

## How to Run
1.  Clone this repository.
2.  Install dependencies:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn
    ```
3.  Open the Jupyter Notebook:
    ```bash
    jupyter notebook Heart_Disease_Risk_Clustering.ipynb
    ```

---
*Note: This project was originally developed as part of the Data Science curriculum at Boston University.*