# **MTL-Trajet Travel Mode Analysis**

This repository explores travel modes using the **MTL-Trajet** dataset through supervised learning and clustering techniques, focusing on classification, clustering, and behavioral analysis.

---

## **Table of Contents**
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Key Features](#key-features)
4. [Modeling Workflow](#modeling-workflow)
5. [Clustering Analysis](#clustering-analysis)
6. [Technologies Used](#technologies-used)
7. [Results and Insights](#results-and-insights)
8. [License](#license)

---

## **Project Overview**
This project leverages machine learning and clustering to predict travel modes and uncover patterns in multimodal travel data. Key challenges like missing data and class imbalance are addressed for robust analysis.

---

## **Dataset**
- **Name**: MTL-Trajet Travel Dataset
- **Source**: [MTL-Trajet Dataset](https://open.canada.ca/data/en/dataset/955de068-9556-4aa1-980e-487b057bbc9d)
- **Description**: Contains travel data including trip purpose, travel modes, speed, and GPS coordinates.
- **Preprocessing**:
  - Removed redundant columns (`id_trip`, `geometry`).
  - Handled missing values using imputation techniques.
  - Encoded categorical features for compatibility with machine learning models.

---

## **Key Features**
- **Supervised Learning**:
  - Models: Neural Networks, Random Forest, XGBoost
  - Addressed class imbalance with **SMOTE**.
- **Clustering Analysis**:
  - **K-Means**: Behavioral clustering by speed and trip purpose.
  - **DBSCAN**: Identifies density-based clusters and outliers.
- **Dimensionality Reduction**:
  - PCA highlights key contributors like travel mode, speed, and trip purpose.

---

## **Modeling Workflow**
1. **Preprocessing**:
   - Removed redundant features (e.g., `geometry`, `id_trip`).
   - Imputed missing values using the mean (numeric) and most frequent (categorical).
   - Encoded categorical variables with one-hot encoding.
2. **Supervised Learning**:
   - Trained models: PyTorch Neural Network, Random Forest, Gradient Boosting (XGBoost), and Decision Tree.
   - Performed hyperparameter tuning using `GridSearchCV` and `RandomizedSearchCV`.
3. **Clustering Analysis**:
   - Applied PCA to reduce data dimensions for visualization.
   - Used **K-Means** and **DBSCAN** for cluster identification.
4. **Evaluation**:
   - Compared models using classification reports (accuracy, F1-score).
   - Visualized clustering results using PCA-reduced dimensions.

---

## **Clustering Analysis**
### **PCA Insights**
- **PCA1**: Differentiates motorized trips by speed.
- **PCA2**: Highlights public transport and work-related trips.

### **Results**
- **K-Means**: 
  - 3 clusters: Motorized trips, walking/cycling, and public transport.
  - Clearly separates behavioral patterns.
- **DBSCAN**: 
  - Identifies natural clusters and outliers.
  - Useful for analyzing unique travel behaviors and anomalies.

---

## **Technologies Used**
- **Languages**: Python
- **Libraries**:
  - Data Processing: `pandas`, `numpy`
  - Machine Learning: `scikit-learn`, `torch`
  - Clustering: `KMeans`, `DBSCAN`
  - Visualization: `matplotlib`, `seaborn`

---

## **Results and Insights**
- **Best Supervised Model**: XGBoost achieved **97% accuracy**.
- **K-Means**: Effectively captured behavioral trends in travel data.
- **DBSCAN**: Identified anomalies and rare behaviors in the dataset.

---

## **License**
This project is licensed under the [MIT License](LICENSE). 

---

## **Contact**
For inquiries, reach out to **Mohammad Yazdizadeh**:
- **GitHub**: [M-Yazdizadeh](https://github.com/M-Yazdizadeh)
