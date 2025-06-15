# Clustering Wine Dataset (MSCS 634 - Lab 3)

## Introduction
This lab explores unsupervised clustering techniques using the **Wine dataset** from the `sklearn` library. The objective was to apply and compare the **K-Means** and **K-Medoids** clustering algorithms and evaluate their effectiveness using metrics such as **Silhouette Score** and **Adjusted Rand Index (ARI)**.

---

## Purpose of the Lab3
The main goals of this lab were to:
- Understand the clustering process and its evaluation.
- Apply two different clustering methods (K-Means and K-Medoids).
- Compare their performance based on metrics and visual analysis.
- Learn when and why to choose one algorithm over the other.

---

## Results Data from the Code Run

| Metric                  | K-Means      | K-Medoids    |
|-------------------------|--------------|--------------|
| Silhouette Score        | 0.2849       | 0.2660       |
| Adjusted Rand Index     | 0.8975       | 0.7263       |

### Insights from the Run Data
- **K-Means outperformed K-Medoids** in both clustering quality and label alignment.
  - The **higher Silhouette Score** of K-Means indicates more compact and distinct clusters.
  - The **ARI of 0.8975** shows strong alignment with the true wine classes.
- **K-Medoids**, while slightly weaker in metrics, is known for being more robust to outliers.
- **Cluster Visualization** revealed that K-Means clusters were more symmetrical and evenly distributed, whereas K-Medoids showed more irregular boundaries.
- The relatively low Silhouette Scores suggest **overlap or ambiguity** in feature space even after standardization.

---

## Implementation Details
- Standardization was applied using **z-score normalization** to scale the features.
- **PCA (Principal Component Analysis)** was used to reduce dimensionality to 2D for cluster visualization.
- Evaluation metrics:
  - **Silhouette Score**: Measures cluster cohesion and separation (higher is better).
  - **Adjusted Rand Index**: Measures how similar the clustering is to true labels (1.0 = perfect match).

---

## Challenges & Decisions
- **K-Medoids required installing** `scikit-learn-extra`, which was not available by default.
- Choosing `k=3` was straightforward since the Wine dataset contains 3 actual classes.
- **Dimensionality reduction** via PCA was needed for visualization but may have introduced some information loss.
- Despite high ARI scores, the low Silhouette values highlight that real-world clustering often involves **trade-offs** between accuracy and structure.

---



## ✅ Conclusion
K-Means proved to be a better fit for this dataset due to its accuracy and simplicity, though K-Medoids could be useful in noisier or less uniform datasets. This lab provided hands-on experience in evaluating clustering algorithms and understanding how to interpret their performance.

