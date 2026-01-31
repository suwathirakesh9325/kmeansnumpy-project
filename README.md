# kmeansnumpy-project
# K-Means Clustering Algorithm

## 📌 Project Overview
This project demonstrates the implementation and analysis of the **K-Means Clustering Algorithm** using Python.  
The algorithm is implemented using **NumPy for mathematical operations** and applied to a **synthetic dataset** to understand how clustering works, how centroids are updated, and how initialization affects results.

The project also includes **visualization of clusters** and a **sensitivity analysis** using the inertia metric.

---

## 🎯 Objectives
- Implement the K-Means clustering algorithm
- Generate a synthetic dataset with three clusters
- Apply K-Means with K = 3
- Visualize cluster assignments and centroids
- Analyze the effect of random centroid initialization using inertia

---

## 📂 Project Structure

kmeans-clustering-algorithm/
│
├── kmeans.py        # Python script implementing the K-Means clustering algorithm
├── README.md        # Project documentation and explanation
└── requirements.txt # (Optional) List of required Python packages

## 🧠 Algorithm Explanation

K-Means is an **unsupervised learning algorithm** that groups data points into K clusters by minimizing the distance between points and their corresponding cluster centroids.

### The algorithm follows these steps:

1. **Centroid Initialization**
   - Randomly select K data points as initial centroids

2. **Assignment Step**
   - Calculate Euclidean distance between each data point and all centroids
   - Assign each data point to the nearest centroid

3. **Update Step**
   - Recalculate each centroid as the mean of all data points assigned to it

4. **Convergence Check**
   - Stop iterations when centroids no longer change significantly

5. **Evaluation**
   - Measure clustering quality using inertia (Sum of Squared Errors)

---

## 📊 Dataset Description

The dataset is generated using `sklearn.datasets.make_blobs` (used only for data creation).

**Parameters:**
- Number of samples: 300
- Number of clusters: 3
- Cluster standard deviations: `[1.0, 2.5, 0.8]`
- Dimensions: 2D

Different cluster variances are used to simulate realistic data distribution.

---

## 📈 Inertia (Evaluation Metric)

Inertia measures how tightly data points are grouped around their centroids.

\[
\text{Inertia} = \sum_{i=1}^{K} \sum (x - \mu_i)^2
\]

- Lower inertia indicates better clustering
- Used to compare different random initializations

---

## 🔁 Sensitivity Analysis

To evaluate robustness:
- The algorithm is run **10 times** with random centroid initialization
- Inertia values from each run are recorded
- Mean and standard deviation of inertia are calculated

This analysis shows how **initial centroid placement influences final clustering results**.

---

## 🖼️ Visualization

The program generates a scatter plot showing:
- Data points colored by their assigned cluster
- Final centroids marked using red **X** symbols

The visualization clearly shows separation between clusters and the final centroid positions.

---

## 🛠️ Technologies Used

| Tool | Purpose |
|-----|--------|
| Python | Programming language |
| NumPy | Numerical computations |
| Matplotlib | Data visualization |
| scikit-learn | Synthetic data generation only |

---

## ⚠️ Limitations
- Requires predefined number of clusters (K)
- Sensitive to initial centroid placement
- Assumes spherical clusters
- Not suitable for non-convex cluster shapes

---

## 🚀 Future Enhancements
- Implement K-Means++ initialization
- Extend clustering to 3D data
- Add silhouette score evaluation
- Compare results with other clustering algorithms

---

## 📌 Conclusion
This project provides a clear understanding of how the K-Means clustering algorithm works in practice. Through visualization and sensitivity analysis, it demonstrates the importance of centroid initialization and highlights how different starting points can lead to different clustering outcomes.

---

## ▶️ How to Run the Project

```bash
python kmeans.py
