# E-commerce Sales Analysis with Machine Learning

This project analyzes online retail transaction data to uncover sales patterns and forecast future revenue using basic statistics and Machine Learning models.

## Overview

The workflow covers the full data science pipeline: loading and cleaning raw e-commerce records, exploring trends, running hypothesis tests across countries, and training regression models to predict total sales per transaction.

## Key Steps

1. **Data Cleaning** — Remove missing values (especially in `CustomerID` and `Description`) and duplicate rows. A `TotalSales` column is created as `Quantity × UnitPrice`.
2. **Exploratory Data Analysis (EDA)** — Monthly sales show a peak in November, likely driven by Black Friday and holiday shopping.
3. **Statistical Testing** — An independent t-test shows that sales in the United Kingdom are significantly higher than in Germany (p-value < 0.05).
4. **Machine Learning** — Two models are trained to predict `TotalSales` using `Quantity`, `UnitPrice`, `Month`, and `DayOfWeek`:
   - **Linear Regression** — RMSE: 303.10, R²: 0.75
   - **Random Forest** — RMSE: 426.43, R²: 0.50

   Linear Regression outperforms Random Forest on this dataset.

## Dataset

The raw dataset is stored in `data/ecommerce-data.csv`. After cleaning, the processed file is saved as `data/ecommerce_clean.csv`.

The data includes invoice details such as product description, quantity, unit price, invoice date, customer ID, and country.

## Notebooks

| Notebook | Description |
|----------|-------------|
| `notebooks/1_coleta.preparacao.dados.ipynb` | Data loading, cleaning, and feature creation |
| `notebooks/3_estatistica_basica.ipynb` | Hypothesis testing (UK vs. Germany) |
| `notebooks/4_modelagem_machine_learning.ipynb` | Linear Regression and Random Forest modeling |

## How to Reproduce

1. Create a virtual environment and install the dependencies:

   ```bash
   pip install pandas scikit-learn scipy numpy jupyter
   ```

2. Run the notebooks in order, starting with data preparation, then statistics, then modeling.

## Tech Stack

- **Python** — pandas, scikit-learn, scipy, NumPy
- **Jupyter Notebook** — interactive analysis and visualization
