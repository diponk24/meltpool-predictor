# Melt Pool Dimension Estimation Using Machine Learning

## Overview
This project predicts melt pool dimensions in laser-based metal additive manufacturing using machine learning.
The objective is to estimate:
- Melt Pool Length
- Melt Pool Width
- Melt Pool Depth
from process parameters and alloy composition data.
Accurate melt pool prediction is important because it affects part quality, microstructure, and mechanical properties.

## Problem Statement
The relationship between laser parameters, material composition, and melt pool geometry is highly nonlinear and difficult to model analytically.
This project investigates whether machine learning models can learn these relationships and provide accurate predictions.

## Input Features
### Process Parameters
- Laser Power (W)
- Travel Velocity (mm/s)
- Beam Diameter

### Material Composition
Elemental composition percentages of alloys, including:
- Iron (Fe)
- Nickel (Ni)
- Chromium (Cr)
- Molybdenum (Mo)
- Other alloying elements

## Target Variables
The models predict:
- Melt Pool Length
- Melt Pool Width
- Melt Pool Depth
Each target variable was treated as a separate regression problem.

## Methodology
The workflow includes:
1. Data preprocessing and quality checks
2. Feature preparation
3. Training multiple regression models
4. Hyperparameter tuning using GridSearchCV
5. Performance evaluation on test data

## Machine Learning Models
The following models were implemented and compared:
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor
These ensemble methods were chosen for their ability to capture nonlinear relationships and feature interactions.

## Model Evaluation
Performance was evaluated using the coefficient of determination (R² score).

Results showed that:
- Melt Pool Width had the highest prediction accuracy
- Melt Pool Length predictions were good
- Melt Pool Depth was more difficult to predict

The lower accuracy for depth suggests that additional features or more data may be required.

## Key Learnings
- Dataset quality and size significantly affect prediction accuracy
- Machine learning can effectively solve engineering prediction problems
- Data preprocessing strongly impacts model performance

## Future Improvements
- Perform feature engineering
- Include additional process parameters
- Explore multi-output regression methods
- Validate predictions using experimental data

## Dataset Note

All data used in this project was collected from publicly available research papers and online sources.
No experiments were conducted as part of this work. The dataset was cleaned, processed, and used solely for learning and academic purposes.
