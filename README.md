# Groundwater Surrogate Modeling Framework

**A reproducible Python framework for predicting groundwater quality parameters from climate data using a hybrid surrogate modeling approach.**

---

## 📌 Overview

This repository contains the complete codebase for the Groundwater Surrogate Modeling Framework, developed as part of an MSc research project at Fachhochschule Erfurt. The framework implements a hybrid, hierarchical surrogate modeling approach that integrates:

- Data quality control
- Exploratory data analysis
- Validation framework
- Baseline models
- Hydrochemical regime detection
- Global ML models
- Local models
- Ensemble modeling
- Uncertainty estimation
- Rule-based Water Quality Index (WQI) calculation

The framework predicts groundwater quality parameters (EC, Nitrate, Iron, Manganese, pH, Chloride, Sulfate) from climate variables (Temperature, Rainfall, SPI-12).

---

## 🏙️ Study Area

| Parameter | Value |
|-----------|-------|
| **Cities** | Cologne, Leipzig, Stuttgart (Germany) |
| **Period** | 2015–2024 |
| **Total Observations** | 661 station-year rows |
| **Total Stations** | 469 |
| **Groundwater Parameters** | EC, Nitrate, Iron, Manganese, pH, Chloride, Sulfate |
| **Climate Variables** | Temperature, Rainfall, SPI-12 |

---

## 🧪 Framework Overview

The framework consists of 11 phases:

| Phase | Description |
|-------|-------------|
| 1 | Data Integration |
| 2 | Data Quality Assessment |
| 3 | Exploratory Data Analysis (EDA) |
| 4 | Validation Framework |
| 5 | Baseline Models |
| 6 | Hydrochemical Regime Detection |
| 7 | Global ML Models |
| 8 | Local Models (per regime) |
| 9 | Ensemble Modeling |
| 10 | Uncertainty Estimation |
| 11 | Rule-Based WQI Calculation |

---

## 📁 Repository Structure

```
Groundwater-Prediction-Product/
│
├── Phase1_Data_Integration/
│   └── Master_Dataset.xlsx
│
├── Phase2_Data_Quality/
│   └── Phase2_Data_Quality.ipynb
│
├── Phase3_EDA/
│   └── Phase3_EDA.ipynb
│
├── Phase4_Validation_Framework/
│   └── Phase4_Validation.ipynb
│
├── Phase5_Baseline_Models/
│   └── Phase5_Baselines.ipynb
│
├── Phase6_Regime_Detection/
│   └── Phase6_Regime_Detection.ipynb
│
├── Phase7_Global_ML_Models/
│   ├── Phase7_Global_ML_Models.ipynb
│   └── models/
│       ├── RF_EC_model.pkl
│       ├── RF_nitrate_model.pkl
│       ├── RF_chloride_model.pkl
│       ├── RF_sulfate_model.pkl
│       ├── RF_pH_model.pkl
│       ├── XGB_EC_model.pkl
│       ├── XGB_nitrate_model.pkl
│       ├── XGB_chloride_model.pkl
│       ├── XGB_sulfate_model.pkl
│       ├── XGB_pH_model.pkl
│       └── scaler.pkl
│
├── Phase8_Local_Models/
│   └── Phase8_Local_Models.ipynb
│
├── Phase9_Ensemble_Modeling/
│   └── Phase9_Ensemble.ipynb
│
├── Phase10_Uncertainty_Estimation/
│   └── Phase10_Uncertainty.ipynb
│
├── Phase11_WQI_Calculation/
│   └── Phase11_WQI.ipynb
│
├── Results/
│   ├── Excel_Files/
│   ├── Plots/
│   └── Reports/
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

### Option 1: Run in Google Colab (Recommended for Beginners)

1. Click on any `.ipynb` file in the repository
2. Click the **"Open in Colab"** badge (if available)
3. Upload `Master_Dataset.xlsx` to the Colab session
4. Run all cells

### Option 2: Run Locally

```bash
# Clone the repository
git clone https://github.com/acharya-aditya92/Groundwater-Prediction-Product.git

# Navigate to the directory
cd Groundwater-Prediction-Product

# Install required packages
pip install -r requirements.txt

# Open Jupyter Notebook
jupyter notebook

📦 Requirements
text
pandas>=1.5.0
numpy>=1.23.0
matplotlib>=3.6.0
seaborn>=0.12.0
scikit-learn>=1.2.0
xgboost>=1.7.0
openpyxl>=3.1.0
joblib>=1.2.0
scipy>=1.9.0
🚀 Usage
Step 1: Prepare Your Data
Ensure your data is in Excel format with the following columns:

Column	Description
City	City name
Station_id	Unique station identifier
Year	Year of measurement
EC	Electrical Conductivity (µS/cm)
nitrate	Nitrate (mg/L)
iron	Iron (mg/L)
manganese	Manganese (mg/L)
pH	pH value
chloride	Chloride (mg/L)
sulfate	Sulfate (mg/L)
temperature	Annual mean temperature (°C)
rainfall	Annual rainfall (mm)
SPI	Standardized Precipitation Index
Step 2: Run the Framework
Open the notebooks in order (Phase 1 → Phase 11) and run all cells.

Step 3: Generate Predictions
Use the trained models to predict groundwater quality for new data.

📊 Results Summary
Model Performance (MAE – Lower is Better)
Parameter	Random Forest	XGBoost	Ensemble
EC	348.5	355.8	352.1
Nitrate	11.8	12.4	12.1
Chloride	34.2	35.9	35.0
Sulfate	122.3	126.1	124.2
pH	0.39	0.42	0.40
Key Findings
Random Forest was the best performing individual model

Rainfall was the most important predictor (dilution effect)

3 hydrochemical regimes were identified

WQI by city: Cologne (0.56), Leipzig (109.43), Stuttgart (130.64)

📝 License
MIT License — See LICENSE file for details.

📧 Contact
Aditya Acharya
MSc Sustainable Engineering of Infrastructure
Fachhochschule Erfurt, Germany
GitHub: acharya-aditya92

📖 Citation
If you use this framework in your research, please cite:
Acharya, A. (2026). Groundwater Surrogate Modeling Framework: A Python-based framework for predicting groundwater quality from climate data. GitHub. https://github.com/acharya-aditya92/Groundwater-Prediction-Product
│
├── requirements.txt
└── README.md
