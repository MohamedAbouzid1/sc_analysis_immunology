# Adipose Tissue Single-Cell Analysis

## Overview

This repository contains code and data for a single-cell RNA sequencing (scRNA-seq) analysis project focused on adipose tissue. The project investigates changes in key cell types, including **macrophages**, **lipid-associated macrophages (LAM cells)**, and **adipocytes**, in relation to **BMI in humans** and **weight in mice**. The analysis is part of ongoing research conducted at the Adlung Lab, UKE.

## Goals

1. Identify and characterize **LAM cells** and their gene signatures across BMI and weight groups.
2. Analyze the relationship between **LAM cells** and **adipocytes** across samples.
3. Perform differential gene expression analysis to identify key markers of **LAM cells** and **mature adipocytes**.
4. Investigate MME (membrane metallo-endopeptidase) expression in macrophages.

## Data

The project utilizes the **white adipose atlas dataset** provided by the Rosen Lab, containing both human and mouse samples. The main data preprocessing and analysis pipeline uses `AnnData` objects for scRNA-seq data management.

### Key Datasets:
- **Macrophages**: Subset data focusing on macrophages with annotated LAM cells and their markers.
- **Adipocytes**: Subset data for mature adipocytes across BMI groups.

### Annotation Features:
- Cell type annotations (macrophages, adipocytes)
- LAM cell markers: TREM2, LPL, CD9, SPP1, etc.
- MME-related gene markers: TNF, IL6, CD36, PLIN2, etc.
- Sample-level metadata, including BMI, species, tissue depot (e.g., SAT, VAT).

## Analysis Pipeline

The project is developed using Python with the following major tools and packages:
- **Scanpy**: For preprocessing, visualization, and clustering.
- **pyDESeq2**: For differential gene expression analysis.
- **Matplotlib** and **Seaborn**: For visualization.
- **Pandas** and **NumPy**: For metadata processing and statistical analysis.

### Main Steps:

1. **Preprocessing**:
   - Quality control (mitochondrial and ribosomal content filtering)
   - Normalization and scaling
   - Subsetting macrophages and adipocytes

2. **LAM Cell Analysis**:
   - Identification of LAM cells based on marker expression
   - LAM score computation using marker genes
   - Cluster analysis to identify LAM cell populations

3. **Differential Expression**:
   - Identification of LAM-specific and MME-related gene signatures
   - Analysis of gene expression changes across BMI groups

4. **Adipocyte Analysis**:
   - Quantification of mature adipocytes per sample
   - Comparison of adipocyte abundance across BMI groups

5. **Visualization**:
   - UMAPs and feature plots for cell populations
   - Violin plots for marker gene expression
   - Heatmaps of differential expression results

## Repository Structure
will be updated later

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/sc_analysis_immunology.git
   cd sc_analysis_immunology
   ```

## Results Highlights

- Clusters of LAM cells and their unique gene expression profiles
- Differential expression analysis showing MME-related markers in macrophages
- Relationship between adipocyte abundance and BMI groups

## Contributors

- **Mohamed Abouzid** (Main Contributor)
- Adlung Lab, UKE

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- Rosen Lab for providing the **white adipose atlas dataset**
- Adlung Lab for guidance and support
