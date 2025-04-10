# Mall Customer Segmentation using K-Means Clustering

## 📌 Project Overview
This project applies **K-Means Clustering** to segment customers from the Mall Customers dataset based on their **Annual Income** and **Spending Score**. The goal is to identify distinct customer groups for better-targeted marketing strategies.

---

## 🔍 Data Preprocessing
- The dataset was first checked for **missing values**, inconsistencies, or outliers.
- ✅ No missing data or significant issues were found — so no cleaning was required.
- We selected relevant **numerical features** for clustering:  
  - `Annual Income (k$)`  
  - `Spending Score (1-100)`

---

## 🤖 Choosing the Optimal Number of Clusters

To find the best value for **k** (number of clusters), we used two popular techniques:

### 1. **Elbow Method**
- Plots the **inertia** (sum of squared distances from each point to its cluster center) for different values of `k`.
- We look for the **"elbow point"** — where the drop in inertia slows down.
- This point shows the best balance between performance and simplicity.
- ✅ The elbow clearly appeared at **k = 5**.

### 2. **Silhouette Score**
- Measures how similar a point is to its own cluster compared to other clusters.
- Score ranges from -1 to +1: higher values mean better clustering.
- We plotted silhouette scores for `k = 2` to `k = 10`.
- ✅ The highest silhouette score also occurred at **k = 5**.

👉 **Both methods agreed on 5 clusters**, confirming that `k = 5` was optimal.

---

## 📊 Clustering Results

We applied **K-Means with 5 clusters** and visualized the customer groups using a 2D scatter plot (scaled data).

### 🔹 Cluster Descriptions (1-line each):
- **Cluster 0**: Medium income and medium spending – balanced, regular customers.  
- **Cluster 1**: High income and high spending – premium, high-value shoppers.  
- **Cluster 2**: Low income and high spending – impulsive or trend-driven buyers.  
- **Cluster 3**: High income and low spending – cautious or uninterested rich customers.  
- **Cluster 4**: Low income and low spending – budget-conscious, price-sensitive group.

---

## 📁 Files Included
- `Mall_Customers.csv` – the dataset.
- `k-means.ipynb` – Jupyter Notebook with all code and visualizations.


---

## ✅ Conclusion
Using both statistical and visual tools, we identified 5 clear customer segments based on spending behavior and income level. These insights can be used to **tailor marketing strategies** and improve **customer engagement**.

