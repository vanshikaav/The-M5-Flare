# The M5 Flare Problem
## Predicting M5+ Solar Flares 24 Hours Before They Happen

### Project Overview
Solar flares are powerful eruptions of energy from the Sun that can disrupt satellite communications, GPS navigation, radio transmissions, and electrical infrastructure on Earth.

This project develops machine learning models to predict whether a solar active region will produce an **M5-class or stronger solar flare within the next 24 hours** using only magnetic-field measurements recorded by NASA's Solar Dynamics Observatory (SDO).

The goal is not only to achieve high predictive performance but also to follow a scientifically sound machine learning workflow, understand model limitations, and interpret the results in the context of space weather forecasting.

---

## Dataset

The dataset contains magnetic-field measurements of solar active regions observed between January 2023 and May 2025.

**Download Dataset:**

https://drive.google.com/drive/folders/10MxgP6r7tehUBvsMJT3ZL4vRwErXvRp

The repository does not include the dataset files directly due to repository size considerations.

---

## Features Used

### Original Magnetic Features
- USFLUX – Total Unsigned Magnetic Flux
- TOTUSJH – Total Unsigned Current Helicity
- TOTUSJZ – Total Unsigned Vertical Current
- MEANALP – Mean Magnetic Twist Parameter
- R_VALUE – Magnetic Flux Near the Polarity Inversion Line
- TOTPOT – Total Free Magnetic Energy
- SAVNCPP – Sum of Absolute Net Currents per Polarity
- AREA_ACR – Active Region Area
- ABSNJZH – Absolute Net Current Helicity

### Engineered Features
- ENERGY_FLUX_RATIO
- ENERGY_DENSITY
- HELICITY_CURRENT_RATIO
- CURRENT_COMPLEXITY
- MAGNETIC_COMPLEXITY

---

## Machine Learning Workflow

1. Exploratory Data Analysis (EDA)
2. Data Cleaning and Preprocessing
3. Class Imbalance Handling
   - Class Weights
   - SMOTE
4. Feature Engineering
5. Model Training and Hyperparameter Tuning
6. Model Evaluation on Unseen Test Data
7. Scientific Interpretation of Results

---

## Models Evaluated

- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting
- XGBoost

---

## Best Model

**XGBoost**

Validation Performance:

| Metric | Score |
|----------|---------:|
| Accuracy | 0.9987 |
| Precision | 0.9600 |
| Recall | 1.0000 |
| F1 Score | 0.9796 |
| ROC-AUC | 1.0000 |

---

## Key Findings

- Solar flare prediction is a highly imbalanced classification problem.
- Traditional accuracy can be misleading when flare events are rare.
- Feature engineering improved overall model performance.
- XGBoost achieved the strongest balance between Recall, F1-score, and ROC-AUC.
- Performance on unseen test data highlighted the challenges of operational flare forecasting and threshold selection.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Imbalanced-Learn (SMOTE)
- XGBoost
- Google Colab

---

## Repository Contents

```text
The-M5-Flare/
│
├── M5_Flare_Prediction.ipynb
├── README.md
├── requirements.txt
└── 

