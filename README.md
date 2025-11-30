# Combined Cycle Power Plant Energy Output Prediction

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)  
![NumPy](https://img.shields.io/badge/NumPy-1.26-green?logo=numpy&logoColor=white)  
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.5-orange?logo=scikitlearn&logoColor=white)  
![Dataset](https://img.shields.io/badge/Dataset-Regression-red)

## Project Overview

This repository contains a Jupyter Notebook implementing a Gradient Descent algorithm to predict the net hourly electrical energy output (EP) of a Combined Cycle Power Plant. The dataset includes 9,568 data points collected over 6 years (2006-2011), with features:  
- **Temperature (T)**  
- **Ambient Pressure (AP)**  
- **Relative Humidity (RH)**  
- **Exhaust Vacuum (V)**  

The goal is to train a linear regression model using Gradient Descent on the training data and generate predictions for the test data. Feature scaling (via StandardScaler) is applied to improve convergence. Various learning rates and iterations are tested for optimization.

Key achievements:  
- Custom Gradient Descent for multi-feature regression.  
- Predictions saved in CSV format without exponential notation.  
- Evaluation based on coefficient of determination (R² score).  

Current as of November 30, 2025.

## Repository Contents

- `Solution (4).ipynb`: Main Jupyter Notebook with:  
  - Data loading (from `train.csv` and `test.csv`).  
  - Gradient Descent implementation (step_gradient, cost, gd functions).  
  - Feature scaling using scikit-learn's StandardScaler.  
  - Model training with tunable learning rate (0.0001) and iterations (1000).  
  - Prediction generation and saving to `predictions.csv`.  

**Note**: The dataset files (`train.csv`, `test.csv`) are not included due to size/privacy; assume they are in the working directory as per the problem statement.

## Dataset Description

- **Training Data**: `train.csv` – Contains X (features) and Y (EP target) for training.  
- **Test Data**: `test.csv` – Features only; predictions are generated for this.  
- Source: Combined Cycle Power Plant dataset (details in README.txt, not included here).  
- Size: 9,568 samples in training.  

## Methods

1. **Gradient Descent**:  
   - Initializes weights (m) and bias (c) to 0.  
   - Computes slopes and updates parameters iteratively.  
   - Cost function: Mean Squared Error (MSE).  
   - Tunable: Learning rate (e.g., 0.0001), Iterations (e.g., 1000).  

2. **Feature Scaling**:  
   - Uses `StandardScaler` from scikit-learn to normalize features, aiding faster convergence.  

3. **Predictions**:  
   - Applies trained model to scaled test data.  
   - Outputs a single-column CSV with non-exponential formatted predictions.  

## Dependencies

Install via pip:  
```bash  
pip install numpy scikit-learn pandas  
