# Experimental Results

This directory contains the experimental results, tables, and figures generated from the proposed **pipeline-centric intrusion detection benchmark framework**.

The experiments evaluate the interaction between:

- **Feature Selection (FS)**
- **Feature Extraction (FE)**
- **Classifier Selection**

under a unified, leakage-free evaluation protocol across three heterogeneous intrusion detection datasets:

- AWID
- UNSW-NB15
- CSE-CIC-IDS2018

The benchmark investigates how different feature-processing strategies influence measurement-data representations and downstream intrusion detection performance.

---

## Directory Structure

```
Results/
│
├── Figures/
│   ├── Figure2.*
│   ├── Figure3.*
│   ├── Figure4.*
│   └── Figure5.*
│
├── Tables/
│   ├── Table2.*
│   ├── Table3.*
│   ├── Table4.*
│   ├── Table5.*
│   ├── Table6.*
│   ├── Table7.*
│   └── Table8.*
│
└── README.md
```

---

# Tables

## Table 2 — Top Performing Pipeline Configurations on AWID

Contains the ten highest-performing combinations of:

```
Feature Selection → Feature Extraction → Classifier
```

ranked according to Macro-F1 performance.

Reported metrics:

- Macro-F1 (mean ± standard deviation)
- Weighted-F1 (mean ± standard deviation)

---

## Table 3 — Top Performing Pipeline Configurations on UNSW-NB15

Reports the ten best-performing pipeline configurations evaluated on the UNSW-NB15 dataset.

The table demonstrates the impact of combining different preprocessing strategies and classifiers under a common evaluation framework.

---

## Table 4 — Top Performing Pipeline Configurations on CSE-CIC-IDS2018

Reports the highest-performing pipeline configurations for the CSE-CIC-IDS2018 dataset.

The results show performance behavior under a larger and more heterogeneous traffic environment.

---

## Table 5 — Feature Selection Performance Across Datasets

Provides an aggregated evaluation of feature-selection methods across all feature-extraction and classifier combinations.

Evaluated feature-selection approaches:

- Variance Threshold (VT)
- ANOVA F-test
- Chi-squared (Chi2)

Reported metrics:

- Macro-F1
- Weighted-F1
- Mean performance
- Standard deviation

---

## Table 6 — Feature Extraction Performance Across Datasets

Provides an aggregated comparison of feature-extraction approaches.

Evaluated feature-extraction methods:

- Principal Component Analysis (PCA)
- Linear Discriminant Analysis (LDA)
- Independent Component Analysis (ICA)
- Truncated Singular Value Decomposition (SVD)

---

## Table 7 — Cross-Dataset Classifier Performance Comparison

Reports classifier performance averaged over all feature-selection and feature-extraction configurations.

Evaluated classifier families include:

### Classical Models

- Logistic Regression (LR)
- Naive Bayes (NB)
- Support Vector Machine (SVM)
- Decision Tree (DT)
- K-Nearest Neighbors (KNN)

### Ensemble Models

- Random Forest (RF)
- Extra Trees (ET)
- Stacking Classifier (STACK)

### Boosting Models

- XGBoost (XGB)
- LightGBM (LGBM)
- CatBoost (CAT)
- Gradient Boosting (GB)

---

## Table 8 — Comprehensive Ablation Study

Provides a controlled comparison between:

```
FS-only
```

and

```
FS → FE
```

configurations.

Reported results include:

- Macro-F1 (mean ± standard deviation)
- Δ Macro-F1 improvement/degradation

The purpose is to quantify the marginal contribution of feature extraction after feature selection.

---

# Figures

## Figure 2 — Classifier Performance Comparison

Visualizes classifier behavior across AWID, UNSW-NB15, and CSE-CIC-IDS2018.

The figure compares classical, ensemble, boosting, and stacking-based approaches.

---

## Figure 3 — Feature Selection Comparison

Illustrates the aggregated contribution of feature-selection strategies:

- VT
- ANOVA
- Chi2

across benchmark datasets.

---

## Figure 4 — Feature Extraction Comparison

Shows the influence of feature-extraction methods:

- PCA
- LDA
- ICA
- SVD

with emphasis on supervised versus unsupervised representation learning.

---

## Figure 5 — Ablation Analysis

Visualizes the contribution of feature extraction after feature selection:

```
FS-only
vs.
FS → FE
```

The figure highlights performance gains and degradation introduced by different extraction strategies.

---

# Evaluation Metrics

The primary evaluation metric is:

## Macro-F1

Macro-F1 is used because intrusion detection datasets commonly contain:

- class imbalance
- multiple attack categories
- varying attack frequencies

Additional metric:

## Weighted-F1

Weighted-F1 provides complementary evaluation by considering class distribution.

Performance values are reported as:

```
mean ± standard deviation
```

from repeated validation experiments.

---

# Reproducibility

The results are generated using the experimental framework described in the manuscript.

The repository structure is designed to support:

- transparent evaluation
- reproducible benchmarking
- comparison of feature-processing strategies
- future extension of the IDS pipeline

