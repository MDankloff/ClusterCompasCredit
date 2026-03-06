# Using SHAP Values for Clustering-based Bias Identification
This repository contains the code associated with our paper: "Using SHAP Values for Clustering-Based Bias Identification." 

# Repository Structure
The repository is organized into 9 Notebooks:

 **Pre-processing Notebooks (3)**:
 
 Data cleaning, computing SHAP values and error labels to set up experimental conditions for the COMPAS and German Credit dataset. 
 
 Includes preliminary visualizations using t-SNE.
        
 **Clustering Notebooks (6)**:
 
Each notebook covers a different clustering approach: K-Means, K-Prototypes, and DBSCAN (3) for each dataset (x2).

Per Clustering notebook:
* Utils for data prep, clustering, results and visualization
* Clustering
* Experimental set-up
* Evaluation results: Chi-square test and Silhouette score
* In-depth Analysis: one-vs-all cluster comparison and t-SNE 

# Paper abstract
A form of AI bias occurs when a model produces higher error rates for specific demographic groups, identifiable through sensitive features (e.g., gender) or proxy features (e.g., income). Explanation methods such as SHAP are used to address biases, but it can be unknown a priori which features lead to higher error rates. The Hierarchical Bias Aware Clustering (HBAC) algorithm is an unsupervised method designed to identify clusters with higher error rates using any combination of features. This study assesses whether including SHAP values in HBAC improves bias identification and explores how different feature sets -- including SHAP values, error labels, sensitive, and regular features -- affect clustering performance. We evaluate cluster quality on three criteria: distinctive error rates, distinctive sensitive features, and general cluster separability. Using the COMPAS and German Credit datasets, we experiment with K-Means, K-Prototypes, and DBSCAN embedded within HBAC. Our results show that SHAP values do not improve bias identification and frequently worsen cluster quality. The best performance is achieved when clustering on sensitive features, particularly with K-Means and K-Prototypes. These findings suggest that SHAP values may have limited utility for identifying bias through error rates, and future work should examine their effectiveness in post hoc bias assessments.

# Getting started
To replicate our experiments, you'll need the following datasets:

**Compas_error_shap_fixed.csv**: Use this dataset to run the clustering analyses in the provided notebooks (compas_K-Means, compas_K-Prototypes, compas_DBSCAN).

**compas-scores-two-years.csv**: Use this original dataset from COMPAS for running the pre-processing notebooks.

**credit_all.csv**: use this dataset to run the clustering notebooks (german_credit_K-Means, german_credit_K-Prototypes, german_credit_DBSCAN).

**german_processed**: use this original dataset from UCI repository to run the pre-processing notebook (German_credit_exploratory) 

# Run the notebook
    git clone https://github.com/MDankloff/ClusterCompasCredit.git

# Contact
This code was developed by Mirthe Dankloff and Emma Beauxis-Aussalet. 

For questions about the paper or code please contact: m.e.dankloff@vu.nl, e.m.a.l.beauxisaussalet@vu.nl.
