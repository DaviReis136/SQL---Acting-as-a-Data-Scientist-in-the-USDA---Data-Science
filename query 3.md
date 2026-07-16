# Query 3 -- Coffee Production Trend Analysis and Forecasting

## Business Request

> **Analyze coffee production trends and determine the total coffee
> production for the year 2011. Generate production forecasts for the
> three years following the last available observation.**

------------------------------------------------------------------------

## Business Objective

The USDA requested an analysis of historical coffee production to better
understand long-term production trends and support future planning
through predictive analytics.

------------------------------------------------------------------------

## SQL Query

``` sql
SELECT
    Year,
    SUM(Value) AS Total
FROM Coffee
GROUP BY Year
ORDER BY Year;
```

------------------------------------------------------------------------

## Purpose

This query aggregates the total coffee production for every available
year in the database. The resulting dataset is later exported to Python,
where it is used to build a Linear Regression model for forecasting
future production.

------------------------------------------------------------------------

## SQL Output (Excerpt)

</SQL>

Output:

| Nº | Year | Total |
| -: | ---: | ----: |
|  1 | 1946 |     8 |
|  2 | 1947 |     8 |
|  3 | 1948 |     7 |
|  4 | 1949 |     5 |
|  5 | 1950 |     9 |
|  6 | 1951 |     9 |
|  7 | 1952 |    10 |
|  8 | 1953 |    10 |
|  9 | 1954 |    12 |
| 10 | 1955 |    10 |
| 11 | 1956 |    11 |
| 12 | 1957 |    18 |
| 13 | 1958 |    10 |
| 14 | 1959 |    12 |
| 15 | 1960 |    13 |
| 16 | 1961 |     8 |
| 17 | 1962 |    13 |
| 18 | 1963 |     6 |
| 19 | 1964 |     9 |
| 20 | 1965 |     7 |
| 21 | 1966 |     8 |
| 22 | 1967 |     5 |
| 23 | 1968 |     5 |
| 24 | 1969 |     4 |
| 25 | 1970 |     4 |
| 26 | 1971 |     2 |
| 27 | 1972 |     3 |
| 28 | 1973 |     3 |
| 29 | 1974 |     1 |
| 30 | 1975 |     1 |
| 31 | 1976 |     2 |
| 32 | 1977 |     2 |
| 33 | 1978 |     1 |
| 34 | 1979 |     2 |
| 35 | 1980 |     1 |
| 36 | 1981 |     2 |
| 37 | 1982 |    10 |
| 38 | 1983 |     2 |
| 39 | 1984 |     1 |
| 40 | 1985 |     1 |
| 41 | 1986 |     3 |
| 42 | 1987 |     1 |
| 43 | 1988 |     2 |
| 44 | 1989 |     3 |
| 45 | 1990 |     2 |
| 46 | 1991 |     2 |
| 47 | 1992 |     2 |
| 48 | 1993 |     2 |
| 49 | 1994 |     4 |
| 50 | 1995 |     5 |
| 51 | 1996 |     6 |
| 52 | 1997 |     9 |
| 53 | 1998 |     9 |
| 54 | 1999 |    10 |
| 55 | 2000 |     8 |
| 56 | 2001 |     8 |
| 57 | 2002 |     7 |
| 58 | 2003 |     8 |
| 59 | 2004 |     5 |
| 60 | 2005 |     8 |
| 61 | 2006 |     7 |
| 62 | 2007 |     7 |
| 63 | 2008 |     8 |
| 64 | 2009 |     8 |
| 65 | 2010 |     8 |
| 66 | 2011 |     7 |
| 67 | 2012 |     7 |
| 68 | 2013 |     8 |
| 69 | 2014 |     7 |
| 70 | 2015 |     6 |
| 71 | 2016 |     5 |

------------------------------------------------------------------------

# Loading the Data into Python

``` python
import pandas as pd

coffee = pd.read_csv("year_total_coffee.csv")
dados = coffee
```

------------------------------------------------------------------------

# Building the Linear Regression Model and Predicting Future Coffee Production

``` </>Python

from sklearn.linear_model import LinearRegression
import matplotlib.pyplot as plt
import numpy as np

# X = years
X = dados[["Year"]]

# y = number of tweets
y = dados["Total"]

# Fit the model
modelo = LinearRegression()
modelo.fit(X, y)

# Predicted values for the existing years
dados["predicted"] = modelo.predict(X)

# Future years
future_years = np.array([[2006], [2007], [2008]])
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
plt.ylabel("total by year")
plt.title("Linear Regression and total Predictions [coffe]")
plt.grid(True)
plt.legend()

plt.show()

print("Predictions:")
for year, value in zip(future_years.flatten(), predictions):
    print(f"{year}: {value:.0f} total by year")

```

------------------------------------------------------------------------

# Data Visualization

<img width="881" height="595" alt="image" src="https://github.com/user-attachments/assets/5bd3d80d-1eb4-429c-8269-87b690bcdc1a" />

------------------------------------------------------------------------

# Business Insight

The SQL analysis successfully summarized annual coffee production and
identified the total production for 2011. Using the historical data, a
Linear Regression model was developed to estimate production for
subsequent years.

These forecasts provide valuable information for production planning,
agricultural policy, resource allocation, and long-term strategic
decision-making.

------------------------------------------------------------------------

# SQL Techniques Used

-   SUM()
-   GROUP BY
-   ORDER BY

------------------------------------------------------------------------

# Python Techniques Used

-   Pandas
-   NumPy
-   Scikit-Learn
-   Linear Regression
-   Matplotlib

------------------------------------------------------------------------

# Skills Demonstrated

-   SQL
-   Data Aggregation
-   Data Analysis
-   Python
-   Machine Learning
-   Predictive Analytics
-   Data Visualization
-   Agricultural Data Science

------------------------------------------------------------------------

# Business Value

This analysis combines SQL and Machine Learning to transform historical
agricultural data into actionable forecasts, supporting proactive
decision-making within the USDA.
