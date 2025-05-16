# Suicide Rate Prediction

A comparative machine-learning study to forecast national suicide rates using nine regression algorithms, Genetic Algorithm–based feature selection, and Principal Component Analysis on both public and custom-curated datasets.

---

## Introduction

Suicide-rate forecasting can inform timely public health interventions. This project evaluates nine regression models—KNN, Random Forest, Decision Tree, MLP, Linear Regression, Ridge Regression, and SVR (linear, polynomial, RBF)—under three preprocessing regimes:

- **Baseline** (no feature manipulation)  
- **Genetic Algorithm–based feature selection**  
- **Principal Component Analysis (PCA)**  

Experiments are performed on:
1. A publicly available [Kaggle dataset](https://www.kaggle.com/datasets/omkargowda/suicide-rates-overview-1985-to-2021) (1985–2021) with feature pruning due to missingness.  
2. A custom dataset (~84 000 records) merged from [WHO](https://www.who.int/data/gho/data/indicators), [IHME](https://vizhub.healthdata.org/gbd-results/?params=gbd-api-2021-public/d224811490bcdc81b32db192a4e9c45a), [World Bank](https://data.worldbank.org/), and national sources for richer socio-demographic indicators.

---

## Features

- Wrapper-based feature selection via a Genetic Algorithm (`GAFeatureSelectionCV`)  
- Dimensionality reduction via PCA retaining 95 % variance  
- Nine regression algorithms implemented in scikit-learn  
- Nested cross-validation to prevent data leakage  
- Comprehensive performance metrics (MAE, MSE, RMSE)  

---

## Datasets

1. **Public Kaggle Dataset** (`first_dataset/`)  
   - 31 756 records, 12 original columns  
   - HDI, population, and raw counts dropped due to missingness or leakage  
2. **Custom-Curated Dataset** (`second_dataset/`)  
   - ~84 000 records, 10 curated features  
   - Integrated from WHO, IHME (GBD 2021), World Bank, and Statbank Greenland  

> **Note:** Raw and preprocessed CSVs are stored in their respective folders.  

---
