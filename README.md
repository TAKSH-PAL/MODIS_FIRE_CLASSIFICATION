# MODIS Fire Types Classification

A comprehensive machine learning project for classifying fire types using MODIS (Moderate Resolution Imaging Spectroradiometer) satellite data with advanced ML algorithms and feature engineering techniques.

## Overview

This project analyzes fire detection data from NASA's MODIS instrument to classify different types of fires based on various atmospheric and environmental parameters. The dataset contains **271,217 fire detection records** from 2021-2023 with detailed information about fire characteristics, satellite observations, and environmental conditions.

The project implements a complete machine learning pipeline including data preprocessing, exploratory data analysis, feature engineering, model training, and comprehensive evaluation using multiple algorithms.

## Dataset

The project includes comprehensive fire classification data spanning three years:
- `FIRE_CLASSIFICATION_2021.csv` - Fire detection records for 2021
- `FIRE_CLASSIFICATION_2022.csv` - Fire detection records for 2022  
- `FIRE_CLASSIFICATION_2023.csv` - Fire detection records for 2023

**Total Dataset Size**: 271,217 records across all three years

### Class Distribution
The dataset shows an imbalanced distribution of fire types:
- **Type 0**: 257,625 records (95.0%)
- **Type 2**: 13,550 records (5.0%)
- **Type 3**: 42 records (<0.1%)

### Data Features

Each record contains the following information:
- **Location**: `latitude`, `longitude`
- **Detection parameters**: `brightness`, `scan`, `track`
- **Temporal data**: `acq_date`, `acq_time`, `daynight`
- **Satellite info**: `satellite`, `instrument`, `version`
- **Fire characteristics**: `confidence`, `bright_t31`, `frp` (Fire Radiative Power)
- **Target variable**: `type` (fire classification label)

## Project Structure

```
MODIS_FIRE_TYPES_CLASSIFICATION/
├── DATASETS/
│   ├── FIRE_CLASSIFICATION_2021.csv
│   ├── FIRE_CLASSIFICATION_2022.csv
│   └── FIRE_CLASSIFICATION_2023.csv
├── MAIN.ipynb
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.7+
- Jupyter Notebook
- Required Python packages:
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn xgboost
  ```

### Machine Learning Models Implemented

The project includes implementation and comparison of multiple ML algorithms:

- **Random Forest Classifier** - Ensemble method for robust classification
- **XGBoost Classifier** - Gradient boosting for high-performance predictions
- **Logistic Regression** - Linear approach for baseline comparison
- **K-Nearest Neighbors (KNN)** - Instance-based learning algorithm

### Feature Engineering & Data Preprocessing

- **Feature Selection**: SelectKBest with f_classif and mutual_info_classif
- **Data Scaling**: StandardScaler for feature normalization
- **Categorical Encoding**: LabelEncoder and OneHotEncoder for categorical variables
- **Data Integration**: Seamless merging of multi-year datasets
- **Class Imbalance Handling**: Analysis and visualization of imbalanced classes

### Usage

1. Clone or download this repository
2. Ensure all required packages are installed
3. Open `MAIN.ipynb` in Jupyter Notebook
4. Run the notebook cells sequentially to:
   - **Data Loading**: Import and merge 271K+ fire detection records from 2021-2023
   - **Exploratory Data Analysis**: Comprehensive statistical analysis and visualization
   - **Data Preprocessing**: Feature engineering, scaling, and encoding
   - **Model Training**: Train and compare multiple ML algorithms
   - **Model Evaluation**: Generate accuracy scores, classification reports, and confusion matrices
   - **Performance Analysis**: Compare model performance and feature importance

## Data Source

The data is derived from NASA's MODIS Fire and Thermal Anomalies product, which provides near real-time active fire detection from the Terra and Aqua satellites. MODIS detects fires using thermal infrared radiation and provides valuable information for fire monitoring and research.

## Fire Types Classification

The MODIS fire classification system categorizes fires into different types (0, 2, 3) based on:
- **Fire Radiative Power (FRP)**: Intensity and energy output measurements
- **Brightness Temperature**: Thermal characteristics at different wavelengths
- **Environmental Conditions**: Atmospheric and meteorological factors
- **Temporal Patterns**: Day/night detection and acquisition timing
- **Geographic Characteristics**: Latitude, longitude, and spatial distribution
- **Satellite Observations**: Scan and track parameters from Terra and Aqua satellites

### Key Features Used for Classification
- Brightness, bright_t31 (brightness temperature)
- Fire Radiative Power (frp)
- Confidence levels
- Scan and track parameters
- Acquisition date and time
- Day/night observations
- Satellite and instrument information

## Model Performance & Evaluation

The project includes comprehensive model evaluation using:
- **Accuracy Score**: Overall classification performance across all models
- **Classification Report**: Detailed precision, recall, and F1-score for each fire type
- **Confusion Matrix**: Visual representation of classification results
- **Feature Importance Analysis**: Understanding key predictive factors
- **Cross-Model Comparison**: Performance benchmarking across different algorithms

## Applications

This fire classification system can be applied to:
- **Forest Fire Monitoring**: Early warning systems and real-time fire risk assessment
- **Agricultural Burn Management**: Distinguishing between natural and controlled burns
- **Climate Change Research**: Long-term fire pattern analysis and trend identification
- **Environmental Impact Assessment**: Understanding fire effects on ecosystems
- **Emergency Response Planning**: Rapid fire type identification for optimized response
- **Satellite Data Analysis**: Automated processing of MODIS thermal anomaly data

## Technical Features

- **Large-Scale Dataset**: Analysis of 271K+ fire detection records
- **Multi-Year Analysis**: Comprehensive coverage across 2021-2023
- **Advanced Feature Engineering**: Statistical and domain-specific feature creation
- **Model Comparison Framework**: Side-by-side performance evaluation
- **Imbalanced Data Handling**: Techniques for dealing with skewed class distributions
- **Visualization Suite**: Rich plotting with matplotlib and seaborn
- **Scalable Processing**: Efficient handling of large satellite datasets

## Data Quality & Completeness

- **No Missing Values**: Complete dataset with 0 null entries across all features
- **No Duplicates**: Clean data with 0 duplicate records
- **Multi-Satellite Coverage**: Data from both Terra and Aqua MODIS instruments
- **Global Coverage**: Fire detection across diverse geographic regions
- **Temporal Continuity**: Consistent daily observations across the study period


