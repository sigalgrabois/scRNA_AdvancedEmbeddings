---
title: "Enhancing K-means Clustering for Single-Cell Data Analysis"
---

# Overview

This project aims to enhance the robustness and adaptability of the K-means clustering algorithm for single-cell RNA-sequencing (scRNA-seq) data analysis, particularly in assessing cellular heterogeneity. We integrate advanced embedding techniques such as Universal Cell Embeddings (UCE) and Cell2Sentence, and compare their performance with traditional PCA and the original data. Additionally, we propose an enhancement to the K-means++ algorithm, adjusting it based on cell density in the dimensional space to better handle high-dimensional, variable density, and complex biological data.

# Background and Motivation

Analyzing scRNA-seq data is essential for advancing our understanding of cell biology, exploring disease mechanisms, and enhancing the drug development process. A fundamental step in scRNA-seq data analysis is cell type clustering, which organizes cells into groups based on gene expression patterns. This initial clustering significantly influences subsequent analyses and interpretations.

# The Problem

Traditional methods for analyzing scRNA-seq data mainly rely on raw gene expression data, which can be noisy and lack comprehensive information. Other self-supervised methods depend on cell type annotations, limiting their applicability to unseen cell types or datasets. Non-zero-shot methods typically require model tuning for each new dataset, making the representations non-universal without re-training, which is inefficient and time-consuming.

# Our Solution

## Advanced Embedding Techniques

- **Universal Cell Embeddings (UCE)**: A self-supervised model that maps single-cell gene expression profiles into a universal embedding space, capturing the vast molecular diversity across different cell types and species.
- **Cell2Sentence**: Another embedding technique for creating meaningful representations of single-cell data.
- **PCA and Original Data**: Used as benchmarks for comparison.

## Enhanced K-means++ Algorithm

We propose modifying the K-means++ algorithm by incorporating cell density in the dimensional space to improve clustering accuracy. This modification ensures that denser areas have a higher impact on the centroid’s new location, enhancing the algorithm's performance in high-dimensional and variable density data.

# Results

## Data Sets Used

- **10K PBMC Data Set**: Includes 11,990 cell samples.
- **Mouse Kidney Data Set**: Includes 35,833 cell samples.

## Evaluation

We evaluate the clustering performance using score accuracy between known labels to the majority of the labels within each cluster. The results show that integrating advanced embedding techniques with the K-means++ algorithm improves clustering accuracy and robustness.

# Conclusion

The integration of advanced embedding techniques with enhanced clustering algorithms holds promise for improving the analysis of heterogeneous cellular data. Future studies should explore the scalability of these methods and their applicability to larger and more diverse datasets.

---
