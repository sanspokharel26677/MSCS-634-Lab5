# MSCS-634-Lab5

# Clustering Techniques Using DBSCAN and Hierarchical Clustering

## Overview
This lab focuses on implementing and analyzing two clustering algorithms: **Hierarchical Clustering** and **DBSCAN** using the Wine dataset. 
The objective is to explore clustering techniques, understand their strengths and weaknesses, and compare their performance using evaluation metrics.

## Steps Performed
1. **Data Preparation & Exploration**
   - Loaded the Wine dataset from `sklearn.datasets`.
   - Explored data structure using summary statistics, histograms, and a correlation heatmap.
2. **Standardization & Dimensionality Reduction**
   - Standardized features using `StandardScaler`.
   - Reduced dimensions using PCA for visualization.
3. **Hierarchical Clustering**
   - Applied Agglomerative Hierarchical Clustering with Ward linkage.
   - Visualized clusters for different numbers of clusters (2, 3, 4, 5).
   - Generated dendrograms to determine optimal cluster counts.
   - Experimented with different linkage methods (average, complete).
4. **DBSCAN Clustering**
   - Applied DBSCAN with different combinations of `eps` and `min_samples`.
   - Visualized clusters and analyzed noise points.
5. **Comparison and Insights**
   - Compared Hierarchical Clustering and DBSCAN using metrics:
     - Silhouette Score
     - Homogeneity Score
     - Completeness Score
   - Created a comparison table and bar chart for visual clarity.

## Key Findings
### Hierarchical Clustering (Ward)
- Produced three meaningful clusters that moderately aligned with the true class labels.
- Metrics:  
  - Silhouette Score: **0.277**  
  - Homogeneity Score: **0.790**  
  - Completeness Score: **0.783**  

### DBSCAN (eps=0.8, min_samples=5)
- Failed to form valid clusters and classified all points as noise.
- Metrics could not be computed meaningfully because there was only one cluster (all noise).

## Conclusion
- **Best Algorithm:** Hierarchical Clustering (Ward)  
- Hierarchical Clustering worked better for this dataset because:
  - It was less sensitive to parameter tuning.
  - It naturally revealed structure and clusters that aligned with the dataset labels.
- **DBSCAN**, while powerful for datasets with irregular cluster shapes, was not suitable for this dataset.

## Enhancements Beyond Requirements
- Added feature distributions, correlation heatmap, and PCA visualizations.
- Explored multiple linkage methods and cluster counts for Hierarchical Clustering.
- Extensively tuned DBSCAN parameters and analyzed noise points.
- Created a comparison table and bar chart for evaluation metrics.
- Added detailed markdown explanations and analysis after each step.

## Challenges and Resolutions
- **DBSCAN parameter sensitivity:** Tried multiple combinations of `eps` and `min_samples` but the algorithm struggled with this dataset.
- **Silhouette Score limitations:** Added error handling when clusters were invalid (only one cluster or all noise).

## Files in Repository
- **Lab5_Notebook.ipynb:** Main Jupyter Notebook containing code, visualizations, and analysis.
- **README.md:** This documentation file summarizing the lab.

## Author
**Sandesh Pokharel**
