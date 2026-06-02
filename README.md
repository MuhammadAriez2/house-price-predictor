# 🏠 House Price Predictor

## Overview
End-to-end machine learning project predicting house sale prices 
using the Ames Housing dataset from Kaggle. Best model achieved 
an R² of 0.90 using Gradient Boosting.

## Tech Stack
Python, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

## Project Structure
- `house_price_predictor.ipynb` — full notebook (EDA → preprocessing → modelling)
- `train.csv` — training data
- `data_description.txt` — description of all 81 features

## Approach
1. **EDA** — analysed SalePrice distribution (skewness 1.88), 
   missing values, and feature correlations
2. **Feature Engineering** — created TotalSF, HouseAge, 
   RemodAge, TotalBathrooms
3. **Preprocessing** — handled missing values, encoded 
   categoricals, scaled features
4. **Modelling** — compared 5 models

## Results
| Model | RMSE | R² |
|---|---|---|
| Gradient Boosting | 0.1369 | 0.8996 |
| Random Forest | 0.1445 | 0.8882 |
| Lasso Regression | 0.1536 | 0.8736 |
| Ridge Regression | 0.1553 | 0.8708 |
| Linear Regression | 0.1559 | 0.8698 |

## Key Findings
- OverallQual and TotalSF were the strongest predictors of price
- SalePrice was right-skewed so log transformation was applied
- Gradient Boosting outperformed linear models by capturing 
  non-linear relationships in the data

## Next Steps
- [ ] Hyperparameter tuning with GridSearchCV
- [ ] Try XGBoost and LightGBM
- [ ] Build a Streamlit app for live price prediction
- [ ] Submit to Kaggle leaderboard
