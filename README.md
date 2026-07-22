# PM2.5-forecasting-palestine
A reproducible benchmark for next-day PM2.5 forecasting in Palestine using statistical, machine learning, and deep learning models.
# PM₂.₅ Forecasting Benchmark for Palestine Using Statistical, Machine Learning, and Deep Learning Models

## Overview

This repository provides the implementation, benchmark dataset, and experimental framework for the paper:

**"A Reproducible Benchmark for Next-Day PM₂.₅ Forecasting in Palestine Using Statistical, Machine Learning, and Deep Learning Models"**

The project presents one of the first comprehensive benchmark studies for PM₂.₅ forecasting in Palestine by systematically comparing statistical, machine learning, and deep learning approaches using identical preprocessing, chronological data splitting, and evaluation procedures.

---

## Repository Structure

```
pm25-forecasting-palestine/

├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_exploratory_data_analysis.ipynb
│   ├── 03_statistical_models.ipynb
│   ├── 04_machine_learning_models.ipynb
│   ├── 05_deep_learning_models.ipynb
│   └── 06_model_evaluation.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── sequence_generator.py
│   ├── train.py
│   ├── evaluate.py
│   └── models.py
│
├── models/
│
├── figures/
│
├── results/
│
├── requirements.txt
├── environment.yml
├── LICENSE
└── README.md
```

---

## Dataset

The benchmark dataset contains daily meteorological observations and PM₂.₅ measurements collected from five monitoring stations in Palestine.

### Variables

- PM₂.₅ (Target)
- Temperature (°C)
- Relative Humidity (%)
- Atmospheric Pressure (hPa)
- Wind Speed (m/s)
- Rainfall (mm)
- Sunshine Duration (hours)
- Month
- Year
- Day
- Day of Week
- Station ID (encoded)

---

## Data Preprocessing

The preprocessing pipeline includes:

- Missing value handling
- Chronological sorting
- Feature engineering
- Station encoding
- Min-Max normalization
- Chronological Train–Validation–Test split (70%-15%-15%)
- Sliding window generation (7-day historical sequences)

---

## Forecasting Models

### Baseline

- Persistence

### Statistical Model

- Linear Regression

### Machine Learning Models

- Random Forest
- Support Vector Regression (SVR)
- XGBoost

### Deep Learning Models

- Long Short-Term Memory (LSTM)
- Gated Recurrent Unit (GRU)
- CNN–LSTM

---

## Evaluation Metrics

The models are evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- Coefficient of Determination (R²)

---

## Experimental Results

| Model | MAE | RMSE | R² |
|--------|------:|------:|------:|
| Persistence | 6.4000 | 9.2335 | 0.0027 |
| Linear Regression | 9.3980 | 13.0875 | -1.0035 |
| Random Forest | 6.8398 | 9.5268 | -0.0616 |
| SVR | 7.8706 | 9.4498 | -0.0445 |
| XGBoost | 7.1793 | 10.3543 | -0.2541 |
| LSTM | 5.7712 | 8.8695 | 0.0798 |
| **GRU** | **6.4548** | **8.6656** | **0.1216** |
| **CNN-LSTM** | **5.7516** | **8.9932** | **0.0540** |

### Summary

- **Lowest MAE:** CNN–LSTM
- **Lowest RMSE:** GRU
- **Highest R²:** GRU

---

## Installation

### Option 1: Using pip

```bash
pip install -r requirements.txt
```

### Option 2: Using Conda

```bash
conda env create -f environment.yml
conda activate pm25_forecasting
```

---

## How to Run

Execute the notebooks in the following order:

```
01_PM_Preparing.ipynb

02_weather_pm_ghg_final_cleaned.ipynb

03_EDA_Figures.ipynb

04_All_Models_evaluation.ipynb



---

## Reproducibility

To ensure reproducibility:

- Fixed random seeds were used where applicable.
- Data were split chronologically to avoid data leakage.
- The same preprocessing pipeline was applied to all models.
- Identical evaluation metrics were used across all experiments.

---

## Software

- Python 3.11
- TensorFlow / Keras
- Scikit-learn
- XGBoost
- NumPy
- Pandas
- Matplotlib
- OpenPyXL

---

## Hardware

Experiments were performed using:

- Apple MacBook Pro (M1)
- Apple M1 Chip
- 8-Core CPU
- 16 GB RAM

---


```
Mohammad Odeh .

A Reproducible Benchmark for Next-Day PM₂.₅ Forecasting in Palestine Using Statistical,
Machine Learning, and Deep Learning Models.

(Under Review)
```

---

## License

This project is released under the MIT License.

---

## Contact

Mohammad Odeh

Email: m.odeh28@student.aaup.edu

GitHub: https://github.com/yourusername
