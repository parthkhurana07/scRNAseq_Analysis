# scRNAseq_Analysis

This project processes and analyzes single-cell RNA-seq (scRNA-seq) data from human peripheral blood mononuclear cells (PBMCs) using the Seurat package. The workflow includes data loading, quality control, normalization, and dimensionality reduction.

## Project Overview

The primary goal of this project is to demonstrate a standard pipeline for analyzing scRNA-seq data using the Seurat framework. The analysis focuses on key steps such as quality control, feature selection, scaling, clustering, and dimensionality reduction.

## Workflow

1. **Data Loading**
   Download dataset.
   ```
   curl -O https://cf.10xgenomics.com/samples/cell-exp/9.0.0/20k_Human_Donor1-4_PBMC_3p_gem-x_multiplex_Multiplex/20k_Human_Donor1-4_PBMC_3p_gem-x_multiplex_Multiplex_count_raw_feature_bc_matrix.h5
   ```
   Load raw scRNA-seq data from an h5 file format.

3. **Seurat Object Creation**  
   Create a Seurat object from raw counts, setting thresholds for minimum cells and features.

4. **Quality Control**  
   - Add mitochondrial content percentage as metadata.  
   - Visualize quality metrics using violin and scatter plots.  
   - Filter low-quality cells based on feature and mitochondrial content thresholds.

5. **Normalization**  
   Normalize gene expression data to prepare for downstream analysis.

6. **Variable Feature Identification**  
   Identify and visualize highly variable features.

7. **Scaling Data**  
   Scale the data to standardize gene expression levels.

8. **Principal Component Analysis (PCA)**  
   Perform PCA to identify the major sources of variation in the dataset. Visualize results with heatmaps and elbow plots.

9. **Clustering**  
   Cluster cells based on PCA results using different resolution parameters.

10. **UMAP Embedding**  
   Visualize clusters in reduced dimensions using UMAP.

## Prerequisites

The following R packages are required:
- [Seurat](https://satijalab.org/seurat/)
- [SeuratObject](https://github.com/satijalab/seurat)
- [tidyverse](https://www.tidyverse.org/)
