# Gene Expression Analysis using Singular Value Decomposition (SVD)

This project performs gene expression analysis using **Singular Value Decomposition (SVD)** on real biological datasets obtained from the **NCBI Gene Expression Omnibus (GEO)**. The objective is to identify underlying biological patterns and tissue-specific expression structures in high-dimensional gene expression data through dimensionality reduction and statistical analysis.

The project demonstrates how linear algebra and data science techniques can be applied to bioinformatics problems for extracting meaningful biological insights from large-scale genomic datasets.

---

## Overview

Gene expression datasets typically contain thousands of genes measured across multiple biological samples, resulting in high-dimensional data that is difficult to interpret directly. Dimensionality reduction techniques such as SVD help identify dominant patterns of variation and reveal relationships between biological samples.

In this project, real gene expression data is downloaded from the NCBI GEO database and processed through a complete analytical pipeline including preprocessing, normalization, dimensionality reduction, and visualization. The resulting principal components are used to analyze tissue-level clustering and biological variability across samples.

The analysis shows that major sources of variation in gene expression correspond to biologically meaningful differences between tissue types.

---

## Dataset

- **Source:** NCBI Gene Expression Omnibus (GEO)
- **Dataset ID:** GSE1133
- **Data Type:** Gene expression microarray data
- **Samples:** Multiple human tissue samples
- **Features:** Thousands of genes per sample

The dataset is automatically downloaded using the `GEOparse` library.

---

## Methodology

The analysis pipeline consists of the following stages:

### 1. Data Acquisition
- Gene expression dataset downloaded directly from NCBI GEO.
- Expression matrix extracted from sample records.

### 2. Data Preprocessing
- Missing values filled using gene-wise mean expression.
- Log2 transformation applied to stabilize variance.
- Invalid or infinite values removed.
- Gene expression values centered across samples.

### 3. Dimensionality Reduction (SVD)
Singular Value Decomposition is applied to the centered data matrix:

X = U Σ Vᵀ


where:
- **U** represents gene loadings,
- **Σ** contains singular values (variance strength),
- **Vᵀ** represents principal component directions.

Principal components capture dominant variation in gene expression.

### 4. Visualization and Analysis
- Scree plot to analyze variance explained by components.
- Projection of samples onto first two principal components.
- Tissue-based clustering visualization.
- Identification of top contributing genes.

---

## Features

- Automatic GEO dataset download
- Gene expression preprocessing pipeline
- Log transformation and normalization
- SVD-based dimensionality reduction
- Variance explained analysis
- Tissue clustering visualization
- Biological interpretation of principal components
- Identification of influential genes

---

## Technologies Used

- Python
- GEOparse
- NumPy
- Pandas
- SciPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## Results

- First few principal components explain a large proportion of total variance.
- Tissue types form distinct clusters in reduced dimensional space.
- Neural tissues separate from metabolic and structural tissues.
- Principal components correspond to biologically meaningful expression patterns.

---
