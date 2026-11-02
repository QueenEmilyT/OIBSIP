# Car Price Prediction Using Machine Learning

**Oasis Infobyte Data Science Internship — Task 3**

**Intern:** Tusiime Emily Queen  
**Track:** Data Science  
**Programming Language:** Python

## 1. Project Overview

This project develops machine learning regression models to predict used-car selling prices based on vehicle characteristics.

The project demonstrates the application of data cleaning, exploratory data analysis, feature engineering, preprocessing, regression modeling, and model evaluation.

## 2. Project Objectives

- Analyze historical used-car selling prices.
- Clean and prepare vehicle data for machine learning.
- Investigate relationships between vehicle characteristics and prices.
- Train Linear Regression and Random Forest models.
- Evaluate predictive performance using MAE, RMSE, and R².
- Identify the best-performing model.
- Interpret model predictions and feature importance.

## 3. Dataset

**Dataset:** CarDekho Used Car Dataset  
**Source:** [Kaggle — Vehicle Dataset from CarDekho](https://www.kaggle.com/datasets/nehalbirla/vehicle-dataset-from-cardekho)

The dataset contains historical used-car listings from India.

The target variable is `selling_price`, measured in Indian rupees (INR).

### Features Used

- `car_age` — Calculated vehicle age
- `km_driven` — Distance traveled
- `brand` — Vehicle manufacturer
- `fuel` — Fuel type
- `seller_type` — Seller category
- `transmission` — Manual or automatic
- `owner` — Ownership history

## 4. Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- Visual Studio Code
- Git and GitHub

## 5. Methodology

### Data Cleaning

The dataset was inspected for missing values, duplicates, invalid numerical values, and inconsistent categorical labels.

### Feature Engineering

Car age was calculated from the manufacturing year using 2026 as the reference year. Car brand was extracted from the vehicle name.

### Exploratory Data Analysis

The analysis included selling-price distributions, box plots by fuel type, scatter plots comparing car age with selling price, a correlation heatmap, and comparisons of prices across vehicle brands.

### Data Preprocessing

Categorical variables were encoded using One-Hot Encoding. Numerical variables were imputed and standardized as appropriate.

The dataset was divided into 80% training data and 20% testing data.

### Model Training

Two regression algorithms were trained:

1. Linear Regression
2. Random Forest Regressor

Both models used preprocessing pipelines fitted on training data.

## 6. Model Evaluation Results

| Model | MAE (INR) | RMSE (INR) | R² |
|---|---:|---:|---:|
| Random Forest | 156,819.27 | 359,726.55 | 0.5983 |
| Linear Regression | 179,642.13 | 384,722.83 | 0.5405 |

### Best-Performing Model

**Random Forest Regressor** achieved the best performance across all three evaluation metrics.

It reduced RMSE by approximately 6.5% compared with Linear Regression and explained approximately 59.83% of the variation in test-set selling prices.

## 7. Feature Importance

Permutation importance analysis identified the following ranking of features:

1. Car age
2. Fuel type
3. Transmission
4. Brand
5. Kilometers driven
6. Seller type
7. Ownership category

Car age made the largest measured contribution to the model's prediction performance.

These importance scores describe model behavior, not causal effects.

## 8. Key Findings

- Random Forest outperformed Linear Regression on the test dataset.
- Car age was the most important feature according to permutation importance.
- The model performed better for many lower-priced vehicles.
- Some expensive vehicles were substantially underpredicted.
- Residual analysis revealed nonconstant prediction error variance.

## 9. Project Limitations

The dataset contains historical Indian used-car prices, so predictions should not be treated as current market valuations.

Important factors such as vehicle condition, maintenance history, and accident records were not available in the selected features.

The models were evaluated using a single train-test split.

## 10. Future Improvements

Potential improvements include cross-validation, hyperparameter tuning, additional vehicle features, logarithmic target transformation, and gradient boosting models.

## 11. How to Run

1. Clone the GitHub repository.
2. Open the `DataScience-Task3-CarPricePrediction` folder.
3. Install the required libraries:

   `pip install pandas numpy matplotlib seaborn scikit-learn jupyter`

4. Download the CarDekho CSV dataset from the source linked above.
5. Place the selected dataset in the `data` directory as `car_details.csv`.
6. Open `Car_Price_Prediction.ipynb` using Jupyter Notebook or VS Code.
7. Run the notebook cells in order. Ensure the file paths match the notebook's working directory.

## 12. Conclusion

The project demonstrated a complete supervised regression workflow, from dataset preparation to model interpretation.

Random Forest was selected as the best-performing model, although additional work would be necessary before deploying the solution for practical vehicle valuation.

## Author

**Tusiime Emily Queen**  
Data Science Intern — Oasis Infobyte

**GitHub:** https://github.com/QueenEmilyT/OIBSIP