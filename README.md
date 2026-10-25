# Ford Car Price Prediction 🚗

## Overview
This project explores Ford car data using Python and machine learning. The notebook includes data inspection, exploratory data analysis, preprocessing, and a Linear Regression model to predict car prices.

## Dataset
The notebook reads `ford.csv`, containing 17,966 rows and 9 columns.

| Feature | Description |
|---|---|
| `model` | Ford car model |
| `year` | Year of manufacture |
| `price` | Car price (target) |
| `transmission` | Transmission type |
| `mileage` | Distance travelled |
| `fuelType` | Fuel type |
| `tax` | Vehicle tax |
| `mpg` | Miles per gallon |
| `engineSize` | Engine size |

## Libraries
- Python
- NumPy and Pandas
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

## Notebook Workflow
1. **Load and inspect data** — view the dataset, descriptive statistics, and missing values.
2. **Explore the data** — visualize the price distribution, numerical correlations, and prices by model, transmission, and fuel type.
3. **Prepare features** — scale numerical columns and one-hot encode selected categorical features.
4. **Train the model** — fit a Linear Regression model using an 80/20 train-test split with `random_state=42`.
5. **Evaluate** — review the R² and Adjusted R² scores.

## Current Model Results
The notebook's reported results are:
- **R²:** 0.4224
- **Adjusted R²:** 0.4180

The final model input in the existing notebook uses one-hot encoded `model` and `fuelType` columns. Although other numerical columns are scaled earlier, they are not used in that final model input.

## How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/1kunal2006/Ford-Car-Price-Prediction.git
   cd Ford-Car-Price-Prediction
   ```
2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib seaborn scikit-learn jupyter
   ```
3. Put `ford.csv` at the path used in the notebook. The current notebook uses `/content/ford.csv`, as commonly used in Google Colab.
4. Open `ford_car_price_prediction.ipynb` in Google Colab or Jupyter Notebook and run the cells in order.

## Future Improvements
- Try additional input features.
- Compare other regression algorithms.
- Evaluate with MAE and RMSE.
- Investigate outliers and improve visualizations.

## Author
**Kunal**

---
*Educational project for practicing data analysis and machine learning.*
