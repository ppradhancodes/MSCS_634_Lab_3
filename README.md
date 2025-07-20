# Lab 3: Clustering Analysis Using K-Means and K-Medoids Algorithms

**Course**: MSCS 634 – Big Data and Data Mining  
**Student Name**: Prafulla Pradhan
**Lab Title**: Clustering on the Wine Dataset  

---

## 🧪 Lab Overview

In this lab, we explore unsupervised machine learning techniques, specifically clustering, using the **Wine dataset** from the `sklearn.datasets` module. The goal is to apply and evaluate **K-Means** and **K-Medoids** algorithms, compare their performance, and visualize the resulting clusters.

This lab enhances understanding of:
- Preprocessing and standardizing datasets for clustering
- Running clustering algorithms with `k=3` (matching known wine classes)
- Evaluating clusters using **Silhouette Score** and **Adjusted Rand Index (ARI)**
- Visualizing clustering output using PCA for 2D projection

---

## 🧭 Steps Performed

1. **Load and explore the Wine dataset**
   - Dataset contains 178 instances with 13 features representing chemical analysis of wines.
   - Class labels represent 3 wine cultivars.

2. **Data preprocessing**
   - Standardized using z-score normalization via `StandardScaler`.

3. **K-Means clustering**
   - Performed clustering using `KMeans` with `k=3`.
   - Calculated Silhouette Score and ARI to assess performance.

4. **K-Medoids clustering**
   - Used `KMedoids` from `scikit-learn-extra` with `k=3`.
   - Computed the same evaluation metrics.

5. **Visualization**
   - Applied **PCA** to project high-dimensional data to 2D.
   - Plotted side-by-side cluster visualizations with centroids and medoids marked.

---

## 📊 Results Summary

| Algorithm   | Silhouette Score | Adjusted Rand Index |
|-------------|------------------|----------------------|
| K-Means     |     0.284859     |       0.897495       |
| K-Medoids   |     0.267622     |       0.741137       |

- **K-Means** had a slightly higher Silhouette Score and ARI, indicating more compact clusters and better alignment with true labels.
- **K-Medoids** was more robust to outliers, as it uses actual data points as medoids.

---

## 🔍 Observations

- K-Means is faster and performs well when clusters are spherical and balanced.
- K-Medoids is preferred when the dataset has noise or outliers, since it’s less sensitive to them.
- PCA visualization showed clear separation of clusters for both methods, with K-Means having slightly tighter boundaries.
- Both models aligned well with the actual class labels (good ARI values).

---

## ⚙️ Dependencies

To run the notebook, install the following libraries:

```bash
pip install scikit-learn matplotlib seaborn scikit-learn-extra
