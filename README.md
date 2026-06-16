# Linear Regression Analysis: The Relationship between MSN Stock Returns and the VN30 Market Index (2020 - 2023)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Data Science](https://img.shields.io/badge/Fields-Quantitative%20Finance%20%7C%20Regression-success)
![Libraries](https://img.shields.io/badge/Libraries-Statsmodels%20%7C%20Pandas%20%7C%20Seaborn-orange)

## 📌 Project Overview
This project conducts a linear regression analysis to evaluate and quantify the statistical relationship between the weekly returns of **MSN (Masan Group)** stock and the **VN30** market index from 2020 to 2023.

This is a practical implementation of a Single-Index Model commonly used in quantitative finance. It aims to determine the systematic risk coefficient ($\beta$) of an individual asset relative to a benchmark market index portfolio.

---

## 🛠️ Tech Stack & Libraries
The analysis is implemented in **Python** using specialized libraries for data manipulation, statistical modeling, and visualization:
* `pandas` & `numpy`: For time-series data wrangling, cleaning, and transformation.
* `statsmodels.api` & `statsmodels.formula.api`: For running Ordinary Least Squares (OLS) regression and executing post-estimation diagnostic tests.
* `matplotlib.pyplot` & `seaborn`: For data visualization, scatter plots, and residual diagnostics.

---

## 📂 Project Structure

The repository is organized cleanly into data and notebook files to maintain reproducible research standards:

```text
├── Data/
│   └── MSN QUAN1.xlsx          # Raw historical weekly dataset containing MSN and VN30 stock prices
├── TheRelationshipbetweenMSNandVN30Returns(2020-2023).ipynb  # Core Jupyter Notebook featuring code and analysis
└── README.md                   # Comprehensive project documentation
