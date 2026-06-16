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

## 📊 Methodology & Modeling

### 1. Data Preparation
* The historical dataset consists of weekly price observations containing `DATE`, `MSN`, and `VN30` metrics.
* Preprocessing includes parsing timestamps (`datetime64`) and configuring the time index to facilitate seamless time-series execution.

### 2. Ordinary Least Squares (OLS) Regression
The regression model is defined as:
$$R_{MSN} = \alpha + \beta \cdot R_{VN30} + \epsilon$$

Where:
* $R_{MSN}$: Return of MSN stock (Dependent Variable).
* $R_{VN30}$: Return of the VN30 index (Independent Variable).
* $\beta$ (Beta): The systematic risk coefficient measuring MSN's sensitivity to overall market movements.

---

## 📉 Statistical Diagnostic Results

Following the model fitting phase, rigorous post-estimation diagnostic tests were conducted to validate the core OLS assumptions:

* **Coefficient of Determination ($R^2$):** Stands at approximately **$30.1\%$**. This indicates that movements in the VN30 market index explain $30.1\%$ of the variance in MSN stock returns. The remaining $69.9\%$ is attributed to idiosyncratic risks unique to the company.
* **Heteroscedasticity Test:** The **Breusch-Pagan** test yielded a $p-value = 0.4967$. Since $p > 0.05$, the null hypothesis of homoscedasticity cannot be rejected, confirming that the error terms have a constant variance.
* **Autocorrelation Test:** The **Durbin-Watson** statistic is close to **$2.0$** ($p = 1.0$), establishing that the residuals are independent and completely free from first-order autocorrelation.
* **Normality Test:** The **Shapiro-Wilk** test returned a $p-value < 0.05$, and the visual Q-Q Plot corroborates that the normality assumption for residuals is rejected. This strongly reflects the **"fat tails"** phenomenon—a classic characteristic inherently present in financial time-series data.

**📌 Key Takeaways:** While the linear model provides excellent foundational market insights, the presence of influential data points during major macro crises (e.g., March 2020 and October 2022) emphasizes that investors should incorporate non-linear risk management frameworks to safeguard against tail-risk and extreme market shocks.

---

## 📂 Project Structure

The repository is organized cleanly into data and notebook files to maintain reproducible research standards:

```text
├── Data/
│   └── MSN QUAN1.xlsx          # Raw historical weekly dataset containing MSN and VN30 stock prices
├── TheRelationshipbetweenMSNandVN30Returns(2020-2023).ipynb  # Core Jupyter Notebook featuring code and analysis
└── README.md                   # Comprehensive project documentation
