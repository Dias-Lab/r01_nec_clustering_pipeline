# r01_nec_clustering_pipeline
Preprocessing, principal component analysis (PCA), and clustering of preliminary NEC dataset

## Description

This pipeline integrates data preprocessing, feature engineering, unsupervised learning techniques (PCA and clustering), and statistical analysis to discover patterns and relationships within the dataset, focusing primarily on clinical outcomes.

Note: The jupyter notebook in this page only shows summary plots and summary statistics, no sample-level data nor IDs are shown in order to protect the privacy and identity of the participants. For the same reason, no patient data was uploaded to this repository.


## Key Steps

1.  **Data Loading and Preprocessing:**

    *   Reads the main dataset and data related to clinical outcomes (e.g., NEC, BPD) from CSV files.
    *   Merges the outcome data and generates binary outcome variables.
    *   Separates the data into initial contact (t0) and follow-up (tN) datasets.

2.  **Feature Engineering:**

    *   Identifies numeric and categorical columns.
    *   Applies one-hot encoding to categorical variables.
    *   Removes constant columns and those with zero variance to improve data quality and model performance.

3.  **Dimensionality Reduction:**

    *   Utilizes Principal Component Analysis (PCA) to reduce the number of dimensions in the dataset.
    *   Analyzes the variance explained by each principal component to understand the data's structure.
    *   Creates scree plots and other visualizations to aid in the selection of the optimal number of principal components.

4.  **Clustering:**

    *   Performs K-means clustering on scaled data to identify distinct groups within the dataset.
    *   Visualizes the clusters using PCA-reduced dimensions for easier interpretation.

5.  **Statistical Analysis:**

    *   Generates histograms for numeric variables by cluster to compare distributions.
    *   Creates stacked bar plots for categorical variables by cluster to analyze group compositions.
    *   Performs proportion tests between clusters to assess the significance of differences in clinical outcome variables.

6.  **Visualization:**

    *   Employs various plotting libraries (e.g., ggplot2) to create visualizations throughout the analysis process, aiding in data exploration and results presentation.

