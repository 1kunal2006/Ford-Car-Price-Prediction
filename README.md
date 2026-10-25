# Ford Car Price Prediction 🚗

## Overview

This project explores a dataset of Ford vehicles and builds a baseline machine-learning model to estimate car prices. The notebook covers data inspection, exploratory data analysis (EDA), preprocessing, model training, and evaluation.

The project is intended as a practical Python data-analysis and machine-learning exercise.

## Objectives

- Explore the structure and quality of the Ford car dataset.
- Visualize car-price distributions and compare prices across categories.
- Examine relationships between numerical features.
- Prepare numerical and categorical features for machine learning.
- Train a Linear Regression baseline and evaluate its predictions.

## Dataset

The notebook expects a CSV file named `ford.csv`. The original dataset contains 17,966 rows and 9 columns:

| Column | Description |
|---|---|
| `model` | Ford vehicle model |
| `year` | Year of manufacture |
| `price` | Vehicle price (prediction target) |
| `transmission` | Transmission type |
| `mileage` | Distance travelled |
| `fuelType` | Fuel type |
| `tax` | Vehicle tax |
| `mpg` | Miles per gallon |
| `engineSize` | Engine size |

Make sure you have permission to use and redistribute the dataset before committing `ford.csv` to a public repository.

## Tools and Libraries

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Workflow

### 1. Data inspection
Load the CSV, review data types and descriptive statistics, and check for missing values.

### 2. Exploratory data analysis
The notebook includes:
- A histogram with a KDE curve to inspect the price distribution.
- A correlation heatmap for numerical features.
- Boxplots comparing prices by model, transmission, and fuel type.

### 3. Preprocessing
Numerical features (`year`, `mileage`, `tax`, `mpg`, and `engineSize`) are scaled, while categorical features (`model`, `transmission`, and `fuelType`) are one-hot encoded. Preprocessing is performed as part of a Scikit-learn pipeline to keep the train/test workflow consistent.

### 4. Model training
A Linear Regression model is trained using an 80/20 train-test split with `random_state=42`.

### 5. Evaluation
The notebook calculates:
- **R²** — proportion of target-price variation explained by the model.
- **Adjusted R²** — R² adjusted for the number of input features.
- **MAE** — mean absolute prediction error.
- **RMSE** — root mean squared prediction error.

Evaluation results are calculated when the notebook is run; they are not presented here as fixed benchmark scores.

## Getting Started

1. Clone the repository:

   ```bash
   git clone https://github.com/1kunal2006/Ford-Car-Price-Prediction.git
   cd Ford-Car-Price-Prediction
   ```

2. Install dependencies:

   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn jupyter
   ```

3. Place `ford.csv` in the project directory. The notebook checks for a local `ford.csv` and also supports the common Google Colab path `/content/ford.csv`.

4. Start Jupyter:

   ```bash
   jupyter notebook
   ```

5. Open `ford_car_price_prediction.ipynb` and run the cells from top to bottom.

## Future Improvements

- Compare Linear Regression with tree-based models such as Random Forest Regressor.
- Tune model parameters and use cross-validation.
- Investigate outliers and potential data-quality issues.
- Add prediction-versus-actual and residual plots.
- Save a trained model and build a simple prediction interface.

## Author

**Kunal**

## License

This repository is shared for educational purposes. Add a license file if you want to define formal permissions for reuse and redistribution.
