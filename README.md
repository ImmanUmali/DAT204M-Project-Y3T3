# DAT204M Project - Product Clustering using the Mercari (MERREC) Dataset

## Overview

This project performs **unsupervised clustering** on products from the **MerRec: A Large-scale Multipurpose Mercari Dataset for Consumer-to-Consumer Recommendation Systems** to identify groups of products with similar customer interaction patterns and product characteristics.

Instead of clustering individual user events, the pipeline first aggregates user behavior at the **product level**, engineers meaningful features, and applies multiple clustering algorithms to compare their performance.

---

# Objectives

- Aggregate user interaction data into product-level metrics.
- Engineer numerical and categorical features representing each product.
- Compare different clustering algorithms.
- Evaluate clustering quality using multiple validation metrics.
- Identify the best-performing clustering model for product segmentation.

---

# Dataset

**Dataset:** https://huggingface.co/datasets/mercari-us/merrec

**Paper:** Li, L., Abi Din, Z., Tan, Z., London, S., Chen, T., & Daptardar, A. (2024). *MerRec: A Large-scale Multipurpose Mercari Dataset for Consumer-to-Consumer Recommendation Systems*. arXiv:2402.14230.

---

# Data Storage

**Platform:** Amazon Web Services S3

**File Format:** Parquet

**Data Layout:**

```text
s3://dat204m-project-g3/
│
├── raw/ -> Contains Raw Data
│   ├── 20230501/
│   ├── 20230601/
│   ├── 20230701/
│   ├── 20230801/
│   ├── 20230901/
│   └── 20231001/
│
├── sampled_eda_data/ -> Contains Cleaned Sample Data
│
├── cleaned_data_final/ -> Contains Cleaned Full Data
│
├── feature_engineered/ -> Contains Feature Engineer Data of Sample Data
│
├── feature_engineered_full/ -> Contains Feature Engineer Data of Full Data
```

---

# Project Workflow

```
Raw Event Data
        │
        ▼
Data Cleaning
        │
        ▼
Exploratory Data Analysis (EDA)
        │
        ▼
Feature Engineering
        │
        ▼
Feature Scaling
        │
        ▼
Clustering
        │
        ▼
Model Evaluation
        │
        ▼
Cluster Analysis
```

---

# Technologies Used

- Python
- PySpark
- Amazon Web Services SageMaker
- Amazon Web Services S3
- Pandas
- NumPy
- Scikit-learn
- Matplotlib

---

# Project Structure

```
.
├── Python Notebooks/
│   ├── BIRCH (Feature Engineered - Full Data).ipynb
│   ├── BIRCH (Feature Engineered - Sample Data).ipynb
│   ├── KMeans (Feature Engineered - Full Data).ipynb
│   ├── KMeans (Feature Engineered - Sample Data).ipynb
│   ├── Gaussian Mixture (Feature Engineered - Full Data).ipynb
│   ├── Gaussian Mixture (Feature Engineered - Sample Data).ipynb
│   ├── Feature Engineered.ipynb
│   └── Feature Engineered (Sample).ipynb
│
├── HTML Files/
│   ├── BIRCH (Feature Engineered - Full Data).html
│   ├── BIRCH (Feature Engineered - Sample Data).html
│   ├── KMeans (Feature Engineered - Full Data).html
│   ├── KMeans (Feature Engineered - Sample Data).html
│   ├── Gaussian Mixture (Feature Engineered - Full Data).html
│   ├── Gaussian Mixture (Feature Engineered - Sample Data).html
│   ├── Feature Engineered.html
│   └── Feature Engineered (Sample).html
│
├── Comprehensive EDA.ipynb
├── Comprehensive EDA.html
│
└── README.md
```
---
# AWS Project Architecture
<img width="7468" height="2488" alt="DAT204M Project AWS arch drawio" src="https://github.com/user-attachments/assets/5029e93a-fea9-4b5b-b9a0-d0c60ea57467" />

---


# Authors 

**Raphael Matthew Azucena**

**Vergel John Himpisao**

**Immanuel Umali**

**Mary Ann Villamor**

**Geilah Tabanao**

