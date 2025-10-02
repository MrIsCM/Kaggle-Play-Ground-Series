# Playground Series S5E10: Road Accident Risk Prediction 🚗💥

## Overview

This project tackles the Kaggle Playground Series Season 5 Episode 10 competition, which focuses on predicting road accident risk based on various road and environmental conditions. The dataset contains synthetic data generated to resemble real-world road accident scenarios, providing features such as road type, weather conditions, lighting, speed limits, and other traffic-related variables.

The challenge involves building a regression model to predict the `accident_risk` score, which represents the likelihood of accidents occurring under specific road and environmental conditions. This type of prediction model has real-world applications in traffic safety management, urban planning, and insurance risk assessment.

## 🎯 Goal and Metric

**Goal:** Predict the accident risk score for different road conditions and environmental factors.

**Target Variable:** `accident_risk` - A continuous value representing the risk level of accidents occurring under given conditions.

**Evaluation Metric:** Root Mean Square Error (RMSE) - The competition evaluates submissions based on the RMSE between predicted and actual accident risk values. Lower RMSE indicates better model performance.


$$
\mathrm{RMSE} = \sqrt{ \frac{1}{n} \sum_{i=1}^{n} \left( y_i - \hat{y}_i \right)^2 }
$$
    
where $y_i$  is the actual accident risk, $ \hat{y}_i $ is the predicted risk, and $ n $ is the number of samples.



## 📁 Project Structure

```
S05E10/
├── data/
│   ├── raw/                    # Original competition data
│   │   ├── train.csv          # Training dataset (517,756 samples)
│   │   ├── test.csv           # Test dataset for predictions
│   │   └── sample_submission.csv
│   ├── processed/             # Cleaned and engineered features
│   └── extension/             # Additional synthetic datasets
│       ├── synthetic_road_accidents_2k.csv
│       ├── synthetic_road_accidents_10k.csv
│       └── synthetic_road_accidents_100k.csv
├── notebooks/
│   ├── 01-eda-initial.ipynb         # Exploratory Data Analysis
│   ├── 02-feature-engineering.ipynb # Feature creation and selection
│   └── 03-modeling.ipynb            # Model training and evaluation
├── src/
│   ├── data/                  # Data processing modules
│   ├── features/              # Feature engineering functions
│   └── models/                # Model implementations
├── models/                    # Saved model artifacts
├── reports/
│   ├── final_report.md        # Competition summary and insights
│   └── figures/               # Visualizations and plots
├── environment.yml            # Conda environment specification
├── requirements.txt           # Python dependencies
└── readme.md                  # This file
```

## 🛠️ Setup

0. Prerequisites:

    * Start by installing [Anaconda](https://www.anaconda.com/download) (or [miniconda](https://www.anaconda.com/docs/getting-started/miniconda/main)) and [git](https://git-scm.com/downloads).

1. Clone this repository:
    ```bash
    git clone <repository-url>
    cd S05E10
    ```

2. Create and activate the conda environment:
    ```bash
    conda env create -f environment.yml
    conda activate kaggle-s5e10
    ```

3. Start executing notebooks/scripts


### Data Setup

The competition data should be placed in the `data/raw/` directory. If you haven't downloaded it yet:

1. Download the data from [Kaggle Competition Page](https://www.kaggle.com/competitions/playground-series-s5e10)
2. Extract the files to `data/raw/`
3. Ensure you have: `train.csv`, `test.csv`, and `sample_submission.csv`
