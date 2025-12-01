# Final Project: Regression Analysis on Housing Prices Dataset

**Author:** Joanna Farris  
**Date:** November 24, 2025  

## Objective
Predict home values using features like overall quality, number of bathrooms and bedrooms, kitchen quality, and neighborhood.  

## Dataset
The dataset contains housing information, including numeric and categorical features related to home characteristics and prices. Key features used in this project:  
- `OverallQual` – Overall quality of the home  
- `FullBath` – Number of full bathrooms  
- `BedroomAbvGr` – Number of bedrooms above ground  
- `Neighborhood` – Neighborhood location  
- `KitchenQual` – Kitchen quality  

## Workflow
1. **Data Exploration** – Checked distributions, missing values, and correlations for selected features.  
2. **Feature Selection & Engineering** – Converted categorical features into numerical format using one-hot encoding. Selected features based on relevance to predicting sale price.  
3. **Model Training** – Trained a Linear Regression model. Split the dataset into training (80%) and test (20%) sets.  
4. **Evaluation** – Measured model performance using R², Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).  
5. **Pipeline Experiments** – Tested two pipelines:  
    - Pipeline 1: Imputer → StandardScaler → Linear Regression  
    - Pipeline 2: Imputer → Polynomial Features (degree=3) → StandardScaler → Linear Regression  
   Compared results to evaluate the impact of preprocessing and feature engineering.  
6. **Reflections & Challenges** – Discussed model performance, overfitting with polynomial features, and potential improvements.  

## Results
| Model / Pipeline | R² | MAE ($) | RMSE ($) |
|-----------------|-----|---------|----------|
| Original Linear Regression | 0.774 | 25,953 | 39,221 |
| Pipeline 1 (Imputer → Scaler → LR) | 0.774 | 25,953 | 39,221 |
| Pipeline 2 (Imputer → Poly → Scaler → LR) | 0.348 | 35,406 | 66,617 |

**Key Findings:**  
- Linear regression with selected features captured ~77% of the variance in home prices.  
- Scaling and imputation helped but didn’t change predictions in Pipeline 1.  
- Polynomial features caused overfitting, worsening performance.  

## Future Work
- Explore additional features such as `LotArea`, `YearBuilt`, `GarageCars`, or `TotalBsmtSF`.  
- Test regularization methods (Ridge, Lasso) to improve generalization.  
- Experiment with tree-based models to capture non-linear relationships without overfitting.  

## Tools
- Python (Pandas, NumPy, Matplotlib, Seaborn)  
- Scikit-Learn for modeling and evaluation  
- Jupyter Notebook for documentation and analysis  

