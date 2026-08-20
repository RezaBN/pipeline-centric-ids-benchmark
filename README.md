# Pipeline-Centric Cross-Dataset Evaluation of Feature Reduction Strategies for Machine Learning-Based Intrusion Detection

![Research Area](https://img.shields.io/badge/Research-Intrusion%20Detection-blue)
![Machine Learning](https://img.shields.io/badge/Method-Machine%20Learning-orange)
![Reproducibility](https://img.shields.io/badge/Focus-Reproducible%20Benchmarking-green)
![Python](https://img.shields.io/badge/Python-3.x-yellow)


## Overview

This repository contains the experimental framework, supplementary materials, and documentation associated with the research study:

**Pipeline-Centric Cross-Dataset Evaluation of Feature Reduction Strategies for Machine Learning-Based Intrusion Detection**

The study investigates the impact of feature reduction strategies on machine-learning-based intrusion detection systems through a controlled, leakage-free, and cross-dataset evaluation framework.

The primary objective is to understand how different dimensionality-reduction strategies influence the effectiveness, robustness, and stability of intrusion detection pipelines when combined with different machine-learning paradigms.

The framework evaluates:

- Feature Selection (FS)
- Feature Extraction (FE)
- Sequential Feature Selection followed by Feature Extraction (FS→FE)
- Classical machine-learning algorithms
- Ensemble learning methods
- Advanced boosting approaches
- Stacking-based meta-learning


---

# Research Motivation

Modern intrusion detection systems operate on high-dimensional network traffic data containing:

- redundant attributes;
- correlated variables;
- irrelevant information;
- imbalanced class distributions;
- heterogeneous traffic patterns.

Although machine-learning approaches have significantly improved intrusion detection performance, reported improvements are often difficult to interpret because feature processing, classifier selection, and dataset characteristics are frequently optimized simultaneously.

This research addresses this challenge through a **pipeline-centric evaluation framework** that separates and analyzes:

1. Data preprocessing;
2. Feature representation transformation;
3. Classification algorithms;
4. Performance evaluation procedures.


The goal is not only to identify high-performing classifiers, but also to understand how feature-reduction strategies affect the information available for automated intrusion detection.


---

# Research Contributions

The main contributions investigated in this repository are:

### 1. Pipeline-Centric Evaluation Framework

A unified experimental pipeline is designed to evaluate feature reduction strategies independently from classifier selection.

### 2. Cross-Dataset Benchmarking

The framework evaluates intrusion detection pipelines across multiple benchmark datasets with different traffic characteristics and attack distributions.

### 3. Leakage-Free Experimental Protocol

All data-dependent operations are performed using training data only, preventing information leakage during preprocessing, feature reduction, and model development.

### 4. Feature Reduction Analysis

The study investigates the individual and combined effects of:

- feature selection;
- feature extraction;
- sequential feature selection and feature extraction.

### 5. Model Family Comparison

The impact of feature reduction is evaluated across multiple learning paradigms, including:

- classical machine learning;
- ensemble learning;
- gradient boosting;
- stacking-based meta-learning.


---

# Experimental Framework

The complete experimental workflow follows the sequence:
