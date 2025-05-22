# 🎓 Student Performance Clustering with K-Means

## 📌 Project Overview

This project explores student academic performance using unsupervised machine learning, specifically K-Means clustering. Students are grouped based on their performance in math, reading, and writing, and these clusters are analyzed in relation to demographic variables such as gender, race/ethnicity, parental education, lunch type, and test preparation course status.

The project demonstrates how clustering can be used to uncover hidden patterns in educational datasets and provide insights into how socio-demographic factors correlate with student success.

---

## 🎯 Objectives

- Group students into clusters based on academic performance
- Visualize and interpret the clusters using PCA (Principal Component Analysis)
- Investigate the relationship between achievement levels and demographic characteristics
- Support data-driven decision making in educational strategy and planning

---

## 📊 Dataset Information

**Source:** `StudentsPerformance.csv`  
**Records:** 1000 students  
**Features:**

- **Performance scores:**
  - `math score`
  - `reading score`
  - `writing score`
- **Demographics:**
  - `gender`
  - `race/ethnicity`
  - `parental level of education`
  - `lunch`
  - `test preparation course`

The dataset is unlabeled, which makes it suitable for clustering tasks rather than classification.

---

## 🧠 Methodology

1. **Data Preprocessing**
   - Selected only performance-related columns for clustering
   - Standardized the data using `StandardScaler`
   - Preserved demographic columns for post-clustering analysis

2. **Clustering**
   - Used the **Elbow Method** to determine the optimal number of clusters
   - Applied **K-Means** clustering (with `n_clusters=3`)
   - Assigned each student to a cluster

3. **Visualization**
   - Reduced dimensions using **PCA** for 2D visualization
   - Created scatterplots to show cluster separation

4. **Demographic Analysis**
   - Explored how cluster membership relates to demographic attributes

---

## 📈 Results

### Cluster Summary

| Cluster | Math Avg | Reading Avg | Writing Avg | Description         |
|---------|----------|-------------|-------------|---------------------|
| 0       | Low      | Low         | Low         | Underperforming     |
| 1       | Medium   | Medium      | Medium      | Average Achievers   |
| 2       | High     | High        | High        | High Performers     |

### Key Insights

- **Gender:** Female students are more prevalent in higher-performing clusters, particularly in reading and writing.
- **Parental Education:** Higher parental education levels correlate with higher student performance.
- **Lunch Type:** Students with free/reduced lunch are more likely to be in low-performing clusters.
- **Test Preparation:** Students who completed a test preparation course are mostly in the high-achievement cluster.

---

## 📊 Visualizations

- PCA-based 2D cluster plot
- Countplots showing demographic distribution across clusters

All plots are created using **matplotlib** and **seaborn**.

---

## 🔧 Technologies Used

- Python 3.x
- pandas
- numpy
- scikit-learn
- seaborn
- matplotlib

To install required libraries:

```bash
pip install pandas numpy scikit-learn seaborn matplotlib

