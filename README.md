# Clustering Mini Project: Apply & Compare Algorithms

Applying and comparing three clustering algorithms on the Mall Customers dataset.

---

## Team

| Name | GitHub |
|---|---|
| Abdulrahman Alnemri | [@AbdulrahmanB-25](https://github.com/AbdulrahmanB-25) |
| Banan Alnemri | [@BananAlnemri](https://github.com/BananAlnemri) |
| Raghad Alsubaie | [@RaghadDasman](https://github.com/RaghadDasman) |
| Saad Alshahrani | [@saadalshahranijob-glitch](https://github.com/saadalshahranijob-glitch) |

---

## Dataset

**Mall Customers Dataset** — [Kaggle](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python)

| Feature | Description |
|---|---|
| Age | Customer age |
| Annual Income (k$) | Annual income in thousands |
| Spending Score (1-100) | Score assigned by the mall based on spending behavior |

200 rows, no missing values, no duplicates.

---

## Algorithms

### K-Means
- Used the **Elbow Method** to pick K=6
- `KMeans(n_clusters=6, init='k-means++', random_state=42)`

### DBSCAN
- `DBSCAN(eps=0.5, min_samples=5)`
- Detects noise points automatically

### Hierarchical Clustering
- `AgglomerativeClustering(n_clusters=4)`

---

## Results

| Algorithm | Clusters | Noise Points | Silhouette Score |
|---|---|---|---|
| K-Means | 6 | 0 | ~0.28 |
| Hierarchical | 4 | 0 | ~0.25 |
| DBSCAN | varies | varies | ~0.35 |

> Scores may vary slightly on each run.

---

## Visualizations

All 4 plots are rendered in a single 2×2 grid:
- Elbow Method
- K-Means clusters
- DBSCAN clusters
- Hierarchical clusters

All cluster plots use PCA to reduce to 2D for visualization.

---

## Conclusion

**K-Means** performed best on this dataset — the data has compact, spherical clusters which suits K-Means well.

| Algorithm | Use When |
|---|---|
| K-Means | Clear round clusters, K is known |
| DBSCAN | Noisy data, unknown K, irregular shapes |
| Hierarchical | Small datasets, need to explore different K values |
