# Query 4 – Honey Production Analysis and Forecasting

## Business Request

> **Calculate the average honey production for 2022 in preparation for a meeting with the Honey Council. Generate production forecasts for the years 2023 and 2030.**

---

## Business Objective

The USDA requested an analysis of honey production to determine the average production in 2022 and estimate future production levels. These insights support strategic planning and discussions with the Honey Council regarding production trends and long-term agricultural policies.

---

## SQL Query

```sql
SELECT
    Year,
    ROUND(AVG(Value), 2) AS Average_Production
FROM Honey
WHERE Year = 2022
GROUP BY Year;
```

---

## Purpose

This query calculates the average honey production for the year 2022 using the `AVG()` aggregate function. The resulting value provides an overview of honey production during the year and serves as the baseline for predictive analysis.

---

## SQL Output

| Year | Average Production |
|----:|-------------------:|
| 2022 | 140.25            |

---

# Loading the Data into Python

```python
import pandas as pd

honey = pd.read_csv("year_average_honey.csv")
dados = honey
```

---

# Building the Linear Regression Model and Predicting Future Honey Production

```</>Python

from sklearn.linear_model import LinearRegression
import matplotlib.pyplot as plt
import numpy as np

# X = years
X = dados[["Year"]]

# y = number of tweets
y = dados["Average"]

# Fit the model
modelo = LinearRegression()
modelo.fit(X, y)

# Predicted values for the existing years
dados["predicted"] = modelo.predict(X)

# Future years
future_years = np.array([[2023], [2030]])
predictions = modelo.predict(future_years)

# Combine historical and future years to draw a single regression line
all_years = np.vstack([X.values, future_years])
regression_line = modelo.predict(all_years)

# Plot
plt.figure(figsize=(10, 6))

# Actual data
plt.scatter(X, y, color="blue", s=60, label="Actual Data")

# Regression line (historical + future)
plt.plot(all_years, regression_line, color="red", linewidth=2, label="Linear Regression")

# Predicted points
plt.scatter(
    future_years,
    predictions,
    color="green",
    marker="X",
    s=120,
    label="Predictions"
)

# Display the predicted value next to each point
for year, value in zip(future_years.flatten(), predictions):
    plt.text(year, value, f"{value:.0f}", fontsize=10,
             ha="left", va="bottom")

plt.xlabel("Year")
plt.ylabel("average by year")
plt.title("Linear Regression and average Predictions [honey]")
plt.grid(True)
plt.legend()

plt.show()

print("Predictions:")
for year, value in zip(future_years.flatten(), predictions):
    print(f"{year}: {value:.0f} average by year")

```

The model learns the historical trend in average honey production and estimates future production values.

---

# Data Visualization

<img width="701" height="495" alt="image" src="https://github.com/user-attachments/assets/81c775f3-a7ed-4951-a82d-cd5b92d464bf" />

---

# Business Insight

The SQL query successfully calculated the average honey production for 2022. Based on historical production data, a Linear Regression model was trained to estimate future production levels.

These projections help the USDA and the Honey Council anticipate future production trends, support resource planning, evaluate long-term agricultural policies, and improve strategic decision-making.

---

# SQL Techniques Used

- AVG()
- ROUND()
- WHERE
- GROUP BY

---

# Python Techniques Used

- Pandas
- NumPy
- Scikit-Learn
- Linear Regression
- Matplotlib

---

# Skills Demonstrated

- SQL
- Data Aggregation
- Statistical Analysis
- Python
- Machine Learning
- Predictive Analytics
- Data Visualization
- Agricultural Data Science

---

# Business Value

This analysis combines SQL and Machine Learning to transform historical honey production data into actionable insights. By integrating descriptive statistics with predictive analytics, the USDA can better anticipate future production patterns and support evidence-based decision-making.
