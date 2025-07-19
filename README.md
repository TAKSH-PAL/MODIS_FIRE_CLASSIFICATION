# MODIS Fire Types Classification

A machine learning project for classifying fire types using MODIS (Moderate Resolution Imaging Spectroradiometer) satellite data.

## Overview

This project analyzes fire detection data from NASA's MODIS instrument to classify different types of fires based on various atmospheric and environmental parameters. The dataset contains fire detection records from 2021-2023 with detailed information about fire characteristics, satellite observations, and environmental conditions.

## Dataset

The project includes fire classification data for three years:
- `FIRE_CLASSIFICATION_2021.csv` - Fire detection records for 2021
- `FIRE_CLASSIFICATION_2022.csv` - Fire detection records for 2022  
- `FIRE_CLASSIFICATION_2023.csv` - Fire detection records for 2023

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
- Required Python packages (to be installed):
  ```bash
  pip install pandas numpy matplotlib seaborn scikit-learn
  ```

### Usage

1. Clone or download this repository
2. Open `MAIN.ipynb` in Jupyter Notebook
3. Run the notebook cells to:
   - Load and explore the MODIS fire data
   - Perform data preprocessing and analysis
   - Build and evaluate fire type classification models
   - Visualize results and insights

## Data Source

The data is derived from NASA's MODIS Fire and Thermal Anomalies product, which provides near real-time active fire detection from the Terra and Aqua satellites. MODIS detects fires using thermal infrared radiation and provides valuable information for fire monitoring and research.

## Fire Types

The classification system categorizes fires into different types based on:
- Fire intensity and radiative power
- Environmental conditions
- Temporal patterns
- Geographic characteristics

## Applications

This classification system can be used for:
- Forest fire monitoring and early warning systems
- Agricultural burn management
- Climate change research
- Environmental impact assessment
- Emergency response planning

