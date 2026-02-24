# Dimensionality-Reduction-Clustering-on-Synthetic-and-Wine-Datasets

# Unsupervised Structure Discovery in High-Dimensional Data

This project investigates how dimensionality reduction and clustering algorithms uncover structure in high-dimensional datasets.

Using both a synthetic nonlinear manifold dataset and the Wine Quality dataset, I evaluate how linear and nonlinear embeddings affect clustering performance and interpretability.

---

## 🔍 Project Objectives

- Compare linear (PCA) and nonlinear (t-SNE, Isomap) dimensionality reduction methods
- Evaluate clustering performance using k-means and DBSCAN
- Analyze how embedding choice impacts cluster recovery
- Investigate whether wine quality labels form natural clusters

---

## 🧪 Part I: Synthetic Nonlinear Manifold

### Data Generation
- Generated five disjoint patches in ℝ²
- Applied a nonlinear mapping into ℝ¹⁰
- Added Gaussian noise to simulate real-world data

### Embedding Methods
- Principal Component Analysis (PCA)
- t-distributed Stochastic Neighbor Embedding (t-SNE)
- Isomap

### Key Findings
- PCA partially separates clusters but fails to capture nonlinear structure
- t-SNE clearly separates all five manifold patches
- Isomap preserves global manifold geometry with minor distortion
- k-means achieves perfect recovery (ARI = 1.0) in raw and t-SNE spaces
- DBSCAN is sensitive to density variation and fails in distorted embedding spaces

This experiment demonstrates how nonlinear embeddings better preserve manifold structure compared to linear projections.

---

## 🍷 Part II: Wine Quality Dataset (6,497 samples)

### Data Preparation
- Combined red and white wine datasets
- Standardized physicochemical features
- Analyzed clustering behavior using wine type and wine quality as references

### Key Findings

#### Wine Type (Red vs White)
- Clear separation using PCA and t-SNE
- k-means achieves high ARI across raw and embedded spaces
- PCA improves silhouette score by reducing noise

#### Wine Quality
- Heavy overlap across all embeddings
- ARI values near zero across clustering methods
- No distinct natural clusters correspond to quality labels

This suggests wine quality is not aligned with low-dimensional geometric structure and is influenced by more complex feature interactions.

---

## 📊 Evaluation Metrics

- Adjusted Rand Index (ARI)
- Silhouette Score

These metrics were used to quantitatively compare clustering performance across embedding spaces.

---

## 🛠 Technologies Used

- Python
- NumPy
- scikit-learn
- Matplotlib
- Pandas
- Overleaf

---

## 💡 Key Takeaways

- Nonlinear dimensionality reduction methods reveal structure not captured by linear PCA.
- Clustering performance depends heavily on embedding choice.
- k-means performs well on compact, well-separated clusters.
- DBSCAN is sensitive to density variation and embedding distortion.
- Not all labels (e.g., wine quality) correspond to natural geometric clusters.

---

## 📌 Conclusion

This project demonstrates how dimensionality reduction techniques influence clustering outcomes in high-dimensional spaces and highlights the importance of geometric structure when applying unsupervised learning methods.
