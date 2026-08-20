# Pipeline-Centric Cross-Dataset Evaluation of Feature Reduction Strategies for Machine Learning-Based Intrusion Detection

## Overview

This repository contains the experimental framework, supplementary
materials, and documentation associated with the research study:

**Pipeline-Centric Cross-Dataset Evaluation of Feature Reduction
Strategies for Machine Learning-Based Intrusion Detection**

The study investigates the impact of feature reduction strategies on
machine-learning-based intrusion detection systems through a controlled,
leakage-free, and cross-dataset evaluation framework.

The framework evaluates:

-   Feature Selection (FS)
-   Feature Extraction (FE)
-   Sequential Feature Selection followed by Feature Extraction (FS→FE)
-   Classical machine-learning models
-   Ensemble learning models
-   Boosting algorithms
-   Stacking-based meta-learning

## Research Motivation

Modern intrusion detection systems operate on high-dimensional network
traffic data containing redundant attributes, correlated variables,
irrelevant information, and imbalanced class distributions.

This research addresses the challenge of understanding how feature
representation affects intrusion detection performance through a
pipeline-centric evaluation framework separating:

1.  Data preprocessing;
2.  Feature reduction;
3.  Classification;
4.  Performance evaluation.

## Experimental Framework

The workflow follows:

    Raw Dataset
         |
         ↓
    Data Preprocessing
         |
         ↓
    Train/Test Stratified Partition
         |
         ↓
    Training-Only Class Balancing
         |
         ↓
    Feature Scaling
         |
         ↓
    Feature Selection
         |
         ↓
    Feature Extraction
         |
         ↓
    Machine Learning Classifier
         |
         ↓
    Performance Evaluation

All data-dependent transformations are fitted exclusively using training
data to prevent information leakage.

## Datasets

The experiments use:

  Dataset           Description
  ----------------- ---------------------------------------
  AWID              Wireless intrusion detection dataset
  UNSW-NB15         Modern network intrusion benchmark
  CSE-CIC-IDS2018   Large-scale network intrusion dataset

Raw datasets are not included due to size and licensing considerations.

## Feature Reduction Strategies

### Feature Selection

-   Variance Threshold (VT)
-   ANOVA F-test
-   Chi-squared (χ²)

### Feature Extraction

-   Principal Component Analysis (PCA)
-   Linear Discriminant Analysis (LDA)
-   Independent Component Analysis (ICA)
-   Truncated Singular Value Decomposition (SVD)

## Classification Models

Evaluated models include:

### Classical Models

-   Decision Tree
-   Logistic Regression
-   K-Nearest Neighbors
-   Naive Bayes
-   Support Vector Machine

### Ensemble Models

-   Random Forest
-   Extra Trees
-   Gradient Boosting

### Advanced Boosting Models

-   XGBoost
-   LightGBM
-   CatBoost

### Meta-Learning

-   Stacking ensemble

## Experimental Evaluation

The framework evaluates:

-   Cross-dataset performance;
-   Feature reduction impact;
-   Model-family interactions;
-   FS-only versus FS→FE pipelines;
-   Performance stability.

Metrics include:

-   Macro F1-score;
-   Weighted F1-score;
-   Accuracy;
-   Macro Precision;
-   Macro Recall.

## Repository Structure

    pipeline-centric-ids-benchmark/

    ├── Datasets/
    ├── Scripts/
    │   ├── preprocessing/
    │   ├── feature_selection/
    │   ├── feature_extraction/
    │   ├── models/
    │   ├── pipelines/
    │   ├── experiments/
    │   ├── evaluation/
    │   └── utils/
    ├── Results/
    ├── Supplementary/
    ├── Documentation/
    └── Notebooks/

## Reproducibility

The repository is designed to support reproducible computational
experiments.

The final release will provide:

-   preprocessing implementations;
-   feature reduction modules;
-   classifier configurations;
-   experimental scripts;
-   evaluation procedures;
-   supplementary documentation.

The experimental protocol follows:

-   fixed random seeds;
-   leakage-free preprocessing;
-   training-only transformation fitting;
-   consistent evaluation across datasets and models.

## Supplementary Materials

Additional information will be provided in:

    Supplementary/

including:

-   dataset descriptions;
-   preprocessing details;
-   feature reduction configurations;
-   model hyperparameters;
-   additional results;
-   ablation-study analysis.

## Citation

Citation information will be added after publication.

## License

This repository is distributed under the license specified in:

    LICENSE

## Contact

Reza BN

GitHub: https://github.com/RezaBN
