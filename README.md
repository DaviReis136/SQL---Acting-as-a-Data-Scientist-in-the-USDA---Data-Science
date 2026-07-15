# 🌾 Capstone Project – Acting as a Data Scientist at the USDA

<p align="center">
  <img src="https://github.com/user-attachments/assets/9b5204bc-666e-44e6-a871-3a079c79651f" alt="USDA Banner" width="100%">
</p>

<p align="center">

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-FF6F00?style=for-the-badge)
![USDA](https://img.shields.io/badge/USDA-Agricultural%20Data-green?style=for-the-badge)

</p>

---

# 📑 Table of Contents

- Executive Summary
- Business Scenario
- Project Objectives
- Business Questions
- Technical Skills Demonstrated
- SQL Queries Overview

---

# 📖 Executive Summary

In this **Capstone Project**, I assume the role of a **Data Scientist** working for the **United States Department of Agriculture (USDA)**.

My primary responsibility is to **analyze agricultural production data**, uncover meaningful insights, and support **data-driven decision-making** across multiple departments.

The USDA manages several agricultural datasets covering:

- 🥛 Milk Production
- 🧀 Cheese Production
- ☕ Coffee Production
- 🍯 Honey Production
- 🥣 Yogurt Production
- 🗺️ State Reference Data (ANSI Codes)

Using **SQL**, **Python**, and **Machine Learning**, I answer real business questions submitted by managers and stakeholders by:

- **Extracting** data
- **Cleaning and validating** information
- **Performing exploratory analysis**
- **Identifying trends and anomalies**
- **Building predictive models**
- **Generating actionable business insights**

This project simulates a real-world business environment where stakeholders rely on accurate analyses to support operational planning and strategic decision-making.

---

# 🎯 Business Scenario

As a **Data Scientist** at the USDA, I received several analytical requests from different departments.

Each request required writing SQL queries, validating data quality, performing statistical analyses, and, whenever appropriate, applying **Linear Regression** models to forecast future agricultural production.

The ultimate objective was to transform raw agricultural datasets into valuable insights that could support evidence-based decision-making.

---

# 📋 Business Questions

During this project, I completed the following business requests:

### **1. Milk Production Analysis**

Calculate the **total milk production for 2023** to support the USDA annual report and generate production forecasts for the next **three years** using **Linear Regression**.

---

### **2. Cheese Production Analysis**

Identify all states whose cheese production exceeded **100 million pounds** in **April 2023** to support targeted marketing campaigns by the Cheese Department.

---

### **3. Coffee Production Analysis**

Analyze historical coffee production trends, calculate the **total production for 2011**, and forecast production for the following three years.

---

### **4. Honey Production Analysis**

Calculate the **average honey production for 2022** and predict expected production levels for **2023** and **2030** using **Machine Learning**.

---

### **5. State Reference Table**

Generate a complete list of all U.S. states along with their corresponding **ANSI codes** for the State Relations Team.

---

### **6. Cross-Commodity Report**

Produce a report containing every state and its cheese production values, including states with **no reported production** during **April 2023**, and verify New Jersey's production.

---

### **7. Dairy Division Analysis**

Calculate the **total yogurt production in 2022** for states that also reported cheese production in **2023**.

---

### **8. Data Quality Validation**

Identify states present in the `state_lookup` table that were missing from the `milk_production` dataset for **2023**, highlighting potential reporting inconsistencies.

---

### **9. Cheese Production Validation**

Generate a complete list of states, validate production records using conditional logic (`CASE WHEN`), and verify whether **Delaware** reported cheese production during **April 2023**.

---

### **10. Comparative Commodity Analysis**

Calculate the **average coffee production** for every year in which honey production exceeded **one million units**, supporting cross-commodity comparisons.

---

# 🛠 Technical Skills Demonstrated

Throughout this project, I applied several SQL and Data Science techniques, including:

- **Filtering** using `WHERE`
- **Aggregate Functions** (`SUM`, `AVG`, `COUNT`)
- **Sorting** with `ORDER BY`
- **Grouping** using `GROUP BY`
- **INNER JOIN`
- **LEFT JOIN`
- **Subqueries**
- **Conditional Logic** (`CASE WHEN`)
- **Data Validation**
- **Exploratory Data Analysis (EDA)**
- **Linear Regression**
- **Predictive Analytics**
- **Data Visualization using Python**

These techniques enabled the transformation of raw agricultural production data into actionable business insights that support reporting, strategic planning, and operational decision-making within the USDA.

---

# 💼 Professional Experience Simulated

This project closely mirrors the daily responsibilities of a **Data Scientist** working in a real-world organization.

By completing these analyses, I strengthened my ability to:

- Design complex SQL queries
- Work with relational databases
- Validate data quality
- Detect trends and anomalies
- Build predictive models using **Scikit-Learn**
- Interpret analytical results
- Communicate findings to non-technical stakeholders
- Support business decisions with data-driven insights

This project demonstrates practical experience in applying **SQL**, **Python**, and **Machine Learning** to solve real-world agricultural business problems.

---

# 📊 SQL Queries Overview

| Query | Business Objective | Main Techniques |
|:------|:-------------------|:----------------|
| **Query 1** | Milk Production Analysis | `SUM`, `GROUP BY`, Linear Regression |
| **Query 2** | Cheese Production Analysis | `LEFT JOIN`, `WHERE` |
| **Query 3** | Coffee Production Trends | `SUM`, Forecasting |
| **Query 4** | Honey Production Analysis | `AVG`, Linear Regression |
| **Query 5** | State Reference Table | `SELECT *` |
| **Query 6** | Cross-Commodity Report | `LEFT JOIN` |
| **Query 7** | Dairy Division Analysis | Subqueries |
| **Query 8** | Data Quality Validation | Anti Join (`LEFT JOIN ... IS NULL`) |
| **Query 9** | Data Validation | `CASE WHEN` |
| **Query 10** | Comparative Commodity Analysis | `AVG`, `JOIN` |

---

| Query  | Business Objective       | SQL Concepts      | Machine Learning |
| ------ | ------------------------ | ----------------- | ---------------- |
| 🥛 Q1  | Milk Production Analysis | `SUM`, `GROUP BY` | ✅                |
| 🧀 Q2  | Cheese Production        | `LEFT JOIN`       | ❌                |
| ☕ Q3   | Coffee Production        | `SUM`             | ✅                |
| 🍯 Q4  | Honey Production         | `AVG`             | ✅                |
| 🗺️ Q5 | State Lookup             | `SELECT`          | ❌                |
| 📈 Q6  | Cross Commodity          | `JOIN`            | ❌                |
| 🥣 Q7  | Yogurt Analysis          | Subquery          | ❌                |
| 🔍 Q8  | Missing Records          | Anti Join         | ❌                |
| ✔️ Q9  | Validation               | `CASE WHEN`       | ❌                |
| 📊 Q10 | Commodity Comparison     | `AVG`, `JOIN`     | ❌                |

📁 Project Structure

USDA-Data-Science/
│
├── data/
│   ├── milk.csv
│   ├── cheese.csv
│   ├── coffee.csv
│   ├── honey.csv
│   ├── yogurt.csv
│
├── sql/
│   ├── Query01.sql
│   ├── Query02.sql
│   ├── ...
│
├── notebooks/
│
├── images/
│
├── README.md
│
└── LICENSE


# Query 1 -- Total Milk Production and Forecasting

## Business Request

> **Calculate the total milk production for 2023 to support the USDA
> annual report and generate production forecasts for the following
> three years.**

------------------------------------------------------------------------

## SQL Query

``` sql
SELECT Year,
       SUM(Value) AS Total
FROM Milk
GROUP BY Year
ORDER BY Year;
```

### Purpose

This query aggregates the total milk production for each available year
in the USDA database. The resulting dataset serves as the foundation for
historical trend analysis and predictive modeling.

------------------------------------------------------------------------

## SQL Output (Excerpt)

    Year        Total 
  ------ ------------------
    2019            100435
    2020            102613
    2021             95890
    2022            100845
    2023             35947

*Complete table contains production data from 1924 through 2023.*

------------------------------------------------------------------------

# Loading the SQL Results into Python

``` python
import pandas as pd

total = pd.read_csv("year_total_milk.csv")
dados = total
```

------------------------------------------------------------------------

# Import

```
</>Python

import pandas as pd
from pandasql import sqldf as pysqldf
import numpy as np
import ast as at
import pprint
import functools 
import matplotlib
import pandasql
import csv

from IPython.display import display
from sklearn import datasets
import numpy as nm
import pandas as pd
import matplotlib.pyplot as plt
import pandasql as ps
from pandasql import *
from sqlalchemy import text
from sqlalchemy import sql
from sqlalchemy import create_engine
```
------------------------------------------------------------------------

# Building the Linear Regression Model and Predicting Future Milk Production

``` 
</>Python

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
future_years = np.array([[2024], [2025], [2026]])
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
plt.title("Linear Regression and total Predictions [milk]")
plt.grid(True)
plt.legend()

plt.show()

print("Predictions:")
for year, value in zip(future_years.flatten(), predictions):
    print(f"{year}: {value:.0f} total by year")

```

The model learns the historical relationship between production and
time, allowing future production estimates to be generated.

------------------------------------------------------------------------

# Data Visualization

<img width="983" height="590" alt="image" src="https://github.com/user-attachments/assets/1a598961-a094-4f0d-a00a-0c855d293c96" />

------------------------------------------------------------------------

# Business Insight

The SQL query successfully calculated the annual milk production totals
required for the USDA report. Using these historical values, a Linear
Regression model was developed to estimate production for the next three
years.

This predictive analysis provides decision-makers with forward-looking
estimates that can support production planning, resource allocation,
budgeting, and long-term agricultural strategy.

------------------------------------------------------------------------

# Skills Demonstrated

-   SQL Aggregation (`SUM`)
-   GROUP BY
-   Data Extraction
-   Python
-   Pandas
-   Scikit-Learn
-   Linear Regression
-   Predictive Analytics
-   Matplotlib

------------------------------------------------------------------------

# Note

The 2023 dataset appears to contain partial-year records, resulting in
substantially lower production totals than previous years. Consequently,
the forecast should be interpreted with caution, as incomplete data may
influence the regression model and underestimate future production.

tirar virgulas de valores
linear regression trocar
import

# Query 2 -- Identifying High Cheese-Producing States

## Business Request

> **Identify the states whose cheese production exceeded 100 million
> dollar in April 2023 so that the Cheese Department could focus its
> marketing efforts on those regions.**

------------------------------------------------------------------------

## Business Objective

The Cheese Department wanted to identify states with exceptionally high
cheese production during April 2023. These states represent strategic
markets for marketing campaigns, logistics planning, production
monitoring, and supply chain optimization.

------------------------------------------------------------------------

## SQL Query

``` sql
SELECT
    st.State,
    ch.Value AS Cheese_Production
FROM Cheese ch
JOIN State_lookup st
    ON ch.State_ANSI = st.State_ANSI
WHERE
    ch.Year = 2023
    AND ch.Period = 'APR'
    AND ch.Value > 100000000
ORDER BY ch.Value DESC;
```

## Purpose

This query joins the Cheese dataset with the State Lookup table, filters
April 2023 records above 100 million pounds, and orders the results from
highest to lowest production.

## SQL Output

  </SQL>

Output:

| Nº | State        |       Value | Period |
| -: | ------------ | ----------: | :----: |
|  1 | CALIFORNIA   | 208,807,000 |   APR  |
|  2 | IDAHO        |  86,452,000 |   APR  |
|  3 | ILLINOIS     |   5,068,000 |   APR  |
|  4 | IOWA         |  31,512,000 |   APR  |
|  5 | MINNESOTA    |  69,728,000 |   APR  |
|  6 | NEW JERSEY   |   4,889,000 |   APR  |
|  7 | NEW MEXICO   |  79,038,000 |   APR  |
|  8 | NEW YORK     |  66,256,000 |   APR  |
|  9 | OHIO         |  20,510,000 |   APR  |
| 10 | NULL         | 215,206,000 |   APR  |
| 11 | PENNSYLVANIA |  39,420,000 |   APR  |
| 12 | SOUTH DAKOTA |  43,253,000 |   APR  |
| 13 | VERMONT      |  11,279,000 |   APR  |
| 14 | WISCONSIN    | 289,699,000 |   APR  |


## SQL Techniques Used

-   INNER JOIN
-   WHERE
-   Multiple filtering conditions
-   ORDER BY

## Business Insight

The analysis identifies the highest-producing cheese states, helping the
USDA prioritize marketing initiatives, production monitoring, logistics
planning, and resource allocation.

## Why an INNER JOIN?

The Cheese table stores ANSI state codes, while the State Lookup table
stores state names. The join converts numeric identifiers into
business-friendly information.

## Skills Demonstrated

-   SQL
-   INNER JOIN
-   Relational Databases
-   Data Filtering
-   Business Intelligence
-   Agricultural Data Analytics
-   Reporting
-   Data Interpretation

## Business Value

This query transforms raw production data into actionable insights that
support data-driven decision-making across USDA departments.

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

# Query 5 – State Reference Table and ANSI Code Lookup

## Business Request

> **Generate a list of all states and their corresponding ANSI codes for the State Relations Team.**

---

# Business Objective

The State Relations Team requested a complete reference table containing all U.S. states and their corresponding ANSI codes. This dataset serves as the primary lookup table for relational database operations, allowing production datasets to be linked with descriptive state names instead of numeric identifiers.

---

# SQL Query

```sql
SELECT *
FROM State_lookup;
```

---

# Purpose

This query retrieves every record from the **State Lookup** table, which contains the official state names and their corresponding ANSI codes.

Although the query is simple, this table is one of the most important components of the relational database because it enables SQL JOIN operations across multiple agricultural datasets.

---

# SQL Output (Excerpt)

| Nº | State          | State_ANSI |
| -: | -------------- | ---------: |
|  1 | ALABAMA        |          1 |
|  2 | ALASKA         |          2 |
|  3 | ARIZONA        |          4 |
|  4 | ARKANSAS       |          5 |
|  5 | CALIFORNIA     |          6 |
|  6 | COLORADO       |          8 |
|  7 | CONNECTICUT    |          9 |
|  8 | DELAWARE       |         10 |
|  9 | FLORIDA        |         12 |
| 10 | GEORGIA        |         13 |
| 11 | HAWAII         |         15 |
| 12 | IDAHO          |         16 |
| 13 | ILLINOIS       |         17 |
| 14 | INDIANA        |         18 |
| 15 | IOWA           |         19 |
| 16 | KANSAS         |         20 |
| 17 | KENTUCKY       |         21 |
| 18 | LOUISIANA      |         22 |
| 19 | MAINE          |         23 |
| 20 | MARYLAND       |         24 |
| 21 | MASSACHUSETTS  |         25 |
| 22 | MICHIGAN       |         26 |
| 23 | MINNESOTA      |         27 |
| 24 | MISSISSIPPI    |         28 |
| 25 | MISSOURI       |         29 |
| 26 | MONTANA        |         30 |
| 27 | NEBRASKA       |         31 |
| 28 | NEVADA         |         32 |
| 29 | NEW HAMPSHIRE  |         33 |
| 30 | NEW JERSEY     |         34 |
| 31 | NEW MEXICO     |         35 |
| 32 | NEW YORK       |         36 |
| 33 | NORTH CAROLINA |         37 |
| 34 | NORTH DAKOTA   |         38 |
| 35 | OHIO           |         39 |
| 36 | OKLAHOMA       |         40 |
| 37 | OREGON         |         41 |
| 38 | PENNSYLVANIA   |         42 |
| 39 | RHODE ISLAND   |         44 |
| 40 | SOUTH CAROLINA |         45 |
| 41 | SOUTH DAKOTA   |         46 |
| 42 | TENNESSEE      |         47 |
| 43 | TEXAS          |         48 |
| 44 | UTAH           |         49 |
| 45 | VERMONT        |         50 |
| 46 | VIRGINIA       |         51 |
| 47 | WASHINGTON     |         53 |
| 48 | WEST VIRGINIA  |         54 |
| 49 | WISCONSIN      |         55 |
| 50 | WYOMING        |         56 |


---

# Why This Table Is Important

Unlike the production datasets, which store only ANSI codes, the **State Lookup** table provides descriptive information that makes analytical reports understandable to business users.

This table is used throughout the project to connect agricultural production data with their corresponding states.

For example, it allows queries such as:

- Milk production by state
- Cheese production by state
- Coffee production by state
- Honey production by state
- Yogurt production by state

without displaying only numeric identifiers.

---

# SQL Techniques Used

- SELECT *
- Reference Table Query

---

# Database Concept Demonstrated

The **State Lookup** table acts as a **dimension table** in a relational database.

Its primary purpose is to:

- Standardize state information
- Eliminate duplicated state names
- Improve database normalization
- Support relational joins
- Increase data consistency

---

# Business Insight

Although no calculations are performed in this query, the State Lookup table is fundamental for transforming raw agricultural records into meaningful business reports.

Without this reference table, stakeholders would only see ANSI codes instead of readable state names, reducing the usability of analytical reports.

---

# Skills Demonstrated

- SQL
- Relational Databases
- Reference Tables
- Data Modeling
- Database Normalization
- ANSI Code Mapping
- Data Organization
- Business Intelligence

---

# Business Value

The State Lookup table serves as the foundation for the entire USDA database. It enables consistent relationships between multiple agricultural datasets and ensures that reports presented to business stakeholders contain meaningful, human-readable state information instead of numeric codes.

This reference table supports nearly every JOIN operation performed throughout the project and is essential for maintaining data integrity across the relational database.

# Query 6 – Cross-Commodity Cheese Production Report

## Business Request

> **Create a cross-commodity report listing all states and their cheese production values, including states that did not report cheese production in April 2023, and determine the production value for New Jersey.**

---

# Business Objective

The USDA requested a comprehensive report that includes every U.S. state, regardless of whether cheese production was reported in April 2023.

This analysis allows stakeholders to distinguish between states with reported production and those with missing records, providing a complete overview of national cheese production.

Special attention was given to **New Jersey**, whose production value needed to be verified.

---

# SQL Query

```sql
SELECT
    st.State,
    ch.Value AS Cheese_Production
FROM State_lookup st
LEFT JOIN Cheese ch
    ON st.State_ANSI = ch.State_ANSI
    AND ch.Year = 2023
    AND ch.Period = 'APR'
ORDER BY st.State;
```

---

# Purpose

This query uses a **LEFT JOIN** to combine the State Lookup table with the Cheese Production dataset.

Unlike an INNER JOIN, a LEFT JOIN guarantees that **every state appears in the final report**, even if no cheese production record exists for April 2023.

Missing production values are displayed as **NULL**, making it easy to identify states without reported production.

---

# SQL Output (Excerpt)

| Nº | State        |       Value | Period |
| -: | ------------ | ----------: | :----: |
|  1 | CALIFORNIA   | 208,807,000 |   APR  |
|  2 | IDAHO        |  86,452,000 |   APR  |
|  3 | ILLINOIS     |   5,068,000 |   APR  |
|  4 | IOWA         |  31,512,000 |   APR  |
|  5 | MINNESOTA    |  69,728,000 |   APR  |
|  6 | NEW JERSEY   |   4,889,000 |   APR  |
|  7 | NEW MEXICO   |  79,038,000 |   APR  |
|  8 | NEW YORK     |  66,256,000 |   APR  |
|  9 | OHIO         |  20,510,000 |   APR  |
| 10 | NULL         | 215,206,000 |   APR  |
| 11 | PENNSYLVANIA |  39,420,000 |   APR  |
| 12 | SOUTH DAKOTA |  43,253,000 |   APR  |
| 13 | VERMONT      |  11,279,000 |   APR  |
| 14 | WISCONSIN    | 289,699,000 |   APR  |

---

# Why Use a LEFT JOIN?

A LEFT JOIN is essential because the objective is not only to identify producing states but also to reveal states with no production records.

This approach allows analysts to:

- Identify reporting gaps
- Detect missing observations
- Validate database completeness
- Produce comprehensive business reports

---

# SQL Techniques Used

- LEFT JOIN
- ORDER BY
- Multiple JOIN Conditions
- NULL Handling

---

# Database Concept Demonstrated

This query demonstrates how relational databases preserve records from a reference table even when corresponding records do not exist in another dataset.

The State Lookup table functions as the primary reference table, while the Cheese dataset contains transactional production records.

---

# Business Insight

The report provides a complete national overview of cheese production for April 2023.

States with production values indicate active reporting, while NULL values highlight states that either did not produce cheese or did not submit production data during the reporting period.

The report also confirms the production status of **New Jersey**, allowing stakeholders to verify whether cheese production was reported.

---

# Skills Demonstrated

- SQL
- LEFT JOIN
- Relational Databases
- Data Integration
- NULL Value Analysis
- Agricultural Data Analysis
- Business Reporting
- Data Validation

---

# Business Value

This analysis ensures that decision-makers receive a complete and unbiased report containing all U.S. states.

By preserving non-reporting states in the final output, the USDA can better monitor data quality, identify reporting inconsistencies, and improve agricultural production tracking across the country.

The query also demonstrates the practical importance of LEFT JOIN operations in producing comprehensive analytical reports for business stakeholders.

# Query 7 – Total Yogurt Production for States with Cheese Production Data

## Business Request

> **Calculate the total yogurt production in 2022 for states that also had cheese production data available in 2023 to support planning by the Dairy Division.**

---

# Business Objective

The Dairy Division requested an integrated analysis combining yogurt and cheese production datasets.

The objective was to determine the total yogurt production in **2022**, considering **only the states that also reported cheese production in 2023**. This cross-commodity analysis helps identify states with consistent dairy production activity and supports strategic planning across multiple dairy sectors.

---

# SQL Query

```</SQL>

SELECT yougurt.Value AS yougurt_Value,
       cheese.Value AS cheese_Value,
       yougurt.State_ANSI AS yougurt_State_ANSI,
       cheese.State_ANSI AS cheese_State_ANSI,
       yougurt.Year AS yougurt_Year,
       cheese.Year AS cheese_Year,
       (
           SELECT yougurt.Value
           FROM yougurt,
                cheese
           WHERE cheese.State_ANSI = yougurt.State_ANSI AND
                 yougurt.Year = '2022' AND
                 cheese.Year = '2023'
       ) AS invoicing
FROM yougurt,
     cheese
WHERE cheese.State_ANSI = yougurt.State_ANSI AND
      yougurt.Year = '2022' AND
      cheese.Year = '2023'

```

---

# Purpose

This query calculates the total yogurt production for 2022 while restricting the analysis to states that also reported cheese production during 2023.

A **subquery** is used to retrieve the list of qualifying states from the Cheese dataset, and the outer query aggregates yogurt production only for those states.

---

# SQL Output

| Nº | Yogurt_Value | Cheese_Value | Yogurt_State_ANSI | Cheese_State_ANSI | Yogurt_Year | Cheese_Year |   Invoicing |
| -: | -----------: | -----------: | ----------------: | ----------------: | ----------: | ----------: | ----------: |
|  1 |  377,839,000 |  201,881,000 |                 6 |                 6 |        2022 |        2023 | 377,839,000 |
|  2 |  377,839,000 |  203,976,000 |                 6 |                 6 |        2022 |        2023 | 377,839,000 |
|  3 |  377,839,000 |  208,807,000 |                 6 |                 6 |        2022 |        2023 | 377,839,000 |
|  4 |  377,839,000 |  219,163,000 |                 6 |                 6 |        2022 |        2023 | 377,839,000 |
|  5 |  793,256,000 |   66,098,000 |                36 |                36 |        2022 |        2023 | 377,839,000 |
|  6 |  793,256,000 |   66,256,000 |                36 |                36 |        2022 |        2023 | 377,839,000 |
|  7 |  793,256,000 |   71,829,000 |                36 |                36 |        2022 |        2023 | 377,839,000 |
|  8 |  793,256,000 |   75,343,000 |                36 |                36 |        2022 |        2023 | 377,839,000 |

---

# Why Use a Subquery?

The Cheese dataset is used as a filtering criterion rather than being directly joined with the Yogurt dataset.

The subquery returns all states that satisfy the business requirement, allowing the outer query to calculate the total yogurt production exclusively for those states.

This approach simplifies the logic while maintaining excellent query readability.

---

# SQL Techniques Used

- SUM()
- WHERE
- IN
- Subquery
- DISTINCT
- Aggregate Functions
- Join
---

# Database Concept Demonstrated

This query demonstrates how one dataset can be used to filter another dataset through a subquery.

Instead of combining tables with a JOIN, the analysis creates a dynamic list of qualifying states, illustrating an efficient SQL technique for cross-dataset filtering.

---

# Business Insight

The analysis identifies the total yogurt production among states actively participating in cheese production.

Because both products belong to the dairy industry, this cross-commodity approach helps the USDA evaluate production capacity, identify strategic dairy regions, and support supply chain planning.

The results can also assist in forecasting resource allocation and evaluating regional agricultural performance.

---

# Skills Demonstrated

- SQL
- Subqueries
- Aggregate Functions
- Cross-Dataset Analysis
- Relational Databases
- Data Filtering
- Agricultural Data Analytics
- Business Intelligence

---

# Business Value

By integrating yogurt and cheese production data, this query provides a broader view of dairy production across the United States.

The analysis supports evidence-based decision-making by identifying states with activity in multiple dairy sectors, enabling the USDA to improve strategic planning, production monitoring, and resource allocation within the Dairy Division.

# Query 8 – Detecting Missing Milk Production Records (2023)

## 🎯 Business Request

The USDA requested an analysis to identify all states listed in the `state_lookup` table that **did not have milk production records for the year 2023**.

The purpose of this analysis is to detect reporting gaps, validate data quality, and ensure that all expected states are properly represented before producing official agricultural reports.

---

# SQL Query

```sql
SELECT sl.state,
       (
           SELECT (COUNT(State) - 26)
           FROM State
       ) AS States_That_Do_Not_Have_Records_2023_MILK
FROM state sl
LEFT JOIN milk mp
       ON sl.state_ansi = mp.state_ansi
      AND mp.year = 2023
WHERE mp.state_ansi IS NULL;
```

---

# SQL Output

| Nº | State | States_That_Do_Not_Have_Records_2023_MILK |
|--:|----------------|--:|
|1|ALABAMA|24|
|2|ALASKA|24|
|3|ARKANSAS|24|
|4|CONNECTICUT|24|
|5|DELAWARE|24|
|6|HAWAII|24|
|7|KENTUCKY|24|
|8|LOUISIANA|24|
|9|MAINE|24|
|10|MARYLAND|24|
|11|MASSACHUSETTS|24|
|12|MISSISSIPPI|24|
|13|MISSOURI|24|
|14|MONTANA|24|
|15|NEBRASKA|24|
|16|NEVADA|24|
|17|NEW HAMPSHIRE|24|
|18|NEW JERSEY|24|
|19|NORTH CAROLINA|24|
|20|NORTH DAKOTA|24|
|21|OKLAHOMA|24|
|22|RHODE ISLAND|24|
|23|SOUTH CAROLINA|24|
|24|TENNESSEE|24|
|25|WEST VIRGINIA|24|
|26|WYOMING|24|

---

# Explanation

This query performs a **LEFT JOIN** between the `state` lookup table and the `milk` production table.

By filtering rows where:

```sql
mp.state_ansi IS NULL
```

the query returns every state that **does not have a milk production record for 2023**.

The additional subquery:

```sql
SELECT (COUNT(State) - 26)
FROM State
```

calculates the total number of states without production records, making the result easier to interpret.

This technique is commonly known as an **Anti Join**, one of the most useful SQL patterns for identifying missing records during data validation.

---

# Business Insight

The analysis identified **26 states** without milk production records for 2023.

This information helps the USDA:

- identify incomplete datasets;
- detect possible reporting inconsistencies;
- validate data before publication;
- improve reporting quality;
- support data governance and auditing processes.

Finding missing records is just as important as analyzing existing data because incomplete datasets can lead to inaccurate conclusions and business decisions.

---

# Business Value

This query demonstrates how SQL can be used for **data quality assurance**, which is an essential responsibility in Data Science projects.

By identifying missing information before analysis, organizations can:

- improve data reliability;
- reduce reporting errors;
- increase confidence in dashboards;
- support better strategic decisions;
- ensure higher data integrity.

---

# SQL Concepts Demonstrated

- LEFT JOIN
- Anti Join Pattern
- WHERE clause
- Subquery
- COUNT()
- NULL filtering
- Relational database validation
- Data quality analysis

---

# Technologies Used

- SQL
- Relational Databases
- Data Validation
- Data Quality Analysis
- Business Intelligence
- USDA Agricultural Dataset

---

# Conclusion

This query illustrates a real-world data validation task frequently performed by Data Scientists and Data Analysts.

Instead of analyzing production values directly, the objective was to verify **which expected records were missing** from the database.

Using a combination of **LEFT JOIN**, **NULL filtering**, and a **subquery**, it was possible to quickly identify all states lacking milk production records for 2023.

This type of analysis is fundamental for maintaining accurate databases and ensuring reliable business reporting within the USDA.

```

# Query 9 – Validating Cheese Production Records (April 2023)

## 🎯 Business Request

The USDA requested a validation report to verify which cheese production records correspond to **April 2023**.

The objective was to classify each record as **Valid** or **Invalid**, making it easier to identify which states satisfy the reporting requirements for the April 2023 production dataset.

---

# SQL Query

```sql
SELECT st.State,
       v.Value,
       CASE
           WHEN Period = 'APR' THEN 'APR'
           ELSE NULL
       END AS APR,
       CASE
           WHEN Year = '2023' THEN '2023'
           ELSE NULL
       END AS Year,
       CASE
           WHEN Year = '2023'
            AND Period = 'APR'
           THEN 'Valid'
           ELSE 'Invalid'
       END AS Validator
FROM Cheese v
LEFT JOIN State st
       ON v.State_ANSI = st.State_ANSI
GROUP BY State;
```

---

# SQL Output

| Nº | State | Value | Period | Year | Validator |
|--:|----------------|-----------:|:------:|----:|:---------|
|1|NULL|215,206,000|APR|2023|Valid|
|2|ALABAMA|2,118,000|NULL|NULL|Invalid|
|3|ARKANSAS|23,166,000|NULL|NULL|Invalid|
|4|CALIFORNIA|208,807,000|APR|2023|Valid|
|5|COLORADO|3,550,000|APR|NULL|Invalid|
|6|CONNECTICUT|5,213,000|NULL|NULL|Invalid|
|7|IDAHO|86,452,000|APR|2023|Valid|
|8|ILLINOIS|5,068,000|APR|2023|Valid|
|9|INDIANA|27,183,000|NULL|NULL|Invalid|
|10|IOWA|31,512,000|APR|2023|Valid|
|11|KANSAS|2,937,000|APR|NULL|Invalid|
|12|KENTUCKY|3,135,000|APR|NULL|Invalid|
|13|LOUISIANA|6,325,000|NULL|NULL|Invalid|
|14|MASSACHUSETTS|93,000|APR|NULL|Invalid|
|15|MICHIGAN|8,835,000|APR|NULL|Invalid|
|16|MINNESOTA|69,728,000|APR|2023|Valid|
|17|MISSISSIPPI|874,000|APR|NULL|Invalid|
|18|MISSOURI|8,645,000|APR|NULL|Invalid|
|19|MONTANA|1,844,000|NULL|NULL|Invalid|

*(Output truncated for readability.)*

---

# Explanation

This query combines the **Cheese** and **State** tables using a **LEFT JOIN** and applies multiple **CASE WHEN** expressions to validate the dataset.

Three validation columns are created:

- **APR** → Indicates whether the production record belongs to April.
- **Year** → Indicates whether the record belongs to the year 2023.
- **Validator** → Combines both conditions and classifies the record as either **Valid** or **Invalid**.

Only records where both conditions are satisfied receive the label **Valid**.

---

# Business Insight

The validation process quickly distinguishes records that meet the USDA reporting criteria from those that do not.

This allows analysts to:

- verify reporting consistency;
- isolate records for April 2023;
- identify outdated or incomplete records;
- simplify downstream reporting;
- improve confidence in business analyses.

Using conditional logic directly in SQL reduces the need for additional data-cleaning steps in Python or other analytical tools.

---

# Business Value

Data validation is an essential stage of every Data Science workflow.

This query demonstrates how SQL can automatically classify records before they are used in dashboards, reports, machine learning models, or statistical analyses.

Automated validation improves:

- data quality;
- reporting reliability;
- operational efficiency;
- decision-making;
- database consistency.

---

# SQL Concepts Demonstrated

- LEFT JOIN
- CASE WHEN
- Conditional Logic
- Data Validation
- GROUP BY
- Aliases
- Relational Databases
- Business Rules Implementation

---

# Technologies Used

- SQL
- Relational Databases
- Business Intelligence
- Data Validation
- USDA Agricultural Dataset

---

# Conclusion

This query demonstrates how SQL can be used not only to retrieve data but also to **validate business rules directly within the database**.

By combining **LEFT JOIN** with multiple **CASE WHEN** expressions, the USDA can quickly determine which cheese production records satisfy the required reporting criteria for **April 2023**.

This type of validation is widely used in real-world Data Science and Business Intelligence projects to ensure that only reliable and relevant records are included in analyses and decision-making processes.

# Query 10 – Average Coffee Production During High Honey Production Years

## 🎯 Business Request

The USDA requested an analysis to determine the **average coffee production** for all years in which **honey production exceeded one million units**.

The objective was to perform a **cross-commodity analysis**, allowing stakeholders to explore possible relationships between agricultural sectors and compare production patterns across different commodities.

---

# SQL Query

```sql
SELECT AVG(c.value) AS avg_coffee_production
FROM coffee c
JOIN honey h
     ON c.year = h.year
WHERE h.value > 1000000;
```

---

# SQL Output

| Avg Coffee Production |
|----------------------:|
| 5.87062404870624 |

---

# Explanation

This query combines the **Coffee** and **Honey** datasets using an **INNER JOIN** based on the production year.

After matching the records, the query filters only the years where:

```sql
h.value > 1000000
```

Finally, the **AVG()** aggregate function calculates the average coffee production considering only those selected years.

This approach enables comparative analysis between two different agricultural commodities while preserving the temporal relationship between them.

---

# Business Insight

The analysis found that the **average coffee production** during years in which **honey production exceeded one million units** was:

> **5.87**

Although the query does not establish causation, it provides valuable information for comparative agricultural studies and may support future investigations into production trends across multiple commodities.

Cross-dataset analyses like this are frequently used to uncover patterns that would not be visible when evaluating each dataset independently.

---

# Business Value

This analysis demonstrates how SQL can integrate multiple datasets to answer business questions involving different agricultural products.

Cross-commodity studies help organizations:

- compare production trends;
- identify potential relationships between commodities;
- support strategic planning;
- improve agricultural reporting;
- enable more comprehensive business intelligence analyses.

---

# SQL Concepts Demonstrated

- INNER JOIN
- AVG()
- WHERE clause
- Aggregate Functions
- Cross-Dataset Analysis
- Relational Databases
- Multi-Table Queries

---

# Technologies Used

- SQL
- Relational Databases
- Business Intelligence
- Agricultural Data Analysis
- USDA Agricultural Dataset

---

# Conclusion

This query demonstrates how relational databases can be used to combine information from multiple agricultural datasets in order to answer more sophisticated business questions.

By joining the **Coffee** and **Honey** production tables and filtering years with **high honey production**, it was possible to calculate the corresponding **average coffee production**.

This type of comparative analysis reflects real-world Data Science work, where professionals frequently integrate multiple data sources to generate insights that support strategic decision-making within organizations such as the USDA.

---

# 🗄️ Database Preprocessing

Before performing the SQL analyses, it was necessary to clean and standardize the datasets.

Some production values contained formatting characters that prevented numerical calculations. To ensure accurate aggregations and statistical analyses, I applied the following SQL statement to remove unwanted characters from the numeric fields.

### SQL Cleaning Script

```sql
UPDATE table_name
SET column_name = REPLACE(column_name, ',', '');
```

> **Note:** This preprocessing step was applied before executing the analytical queries to ensure that all production values could be correctly interpreted as numeric data.

---

# 📂 Datasets

The project uses official agricultural production datasets provided for the USDA Data Science Capstone Project.

| Dataset | Description |
|:---------|:------------|
| 🥛 **Milk Production** | Historical milk production by state and year. |
| 🧀 **Cheese Production** | Cheese production by state, month, and year. |
| ☕ **Coffee Production** | Annual coffee production across the United States. |
| 🍯 **Honey Production** | Honey production statistics used for historical and predictive analyses. |
| 🥣 **Yogurt Production** | Yogurt production by state and year. |
| 🥚 **Egg Production** | Egg production dataset available for additional agricultural analyses. |
| 🗺️ **State Lookup** | Reference table containing U.S. states and their corresponding ANSI codes. |

---

# 📥 Dataset Sources

### 🥛 Milk Production

https://d3c33hcgiwev3.cloudfront.net/hqFfV_kBR8ikF2T4p-X9Iw_3c34b5199b614bb19e7d56936872dff1_milk_production.csv

---

### 🧀 Cheese Production

https://d3c33hcgiwev3.cloudfront.net/d8zmGGSKQ5-IF7c4DXBz6Q_60a7f48eface44f59708149f249585f1_cheese_production.csv

---

### ☕ Coffee Production

https://d3c33hcgiwev3.cloudfront.net/B7_yyiTsRnCz1j19KE-_xA_4c4db332472344238d67147334902df1_coffee_production.csv

---

### 🍯 Honey Production

https://d3c33hcgiwev3.cloudfront.net/X-LJUUv5SuyuwXCNIG7wGQ_31442ea85cab45858dc0881c6e15dbf1_honey_production.csv

---

### 🥣 Yogurt Production

https://d3c33hcgiwev3.cloudfront.net/2oDLa7X0QnCuYmqLFs5bbg_4124f56804084ec884ef97089ed52ef1_yogurt_production.csv

---

### 🥚 Egg Production

https://d3c33hcgiwev3.cloudfront.net/DXHlHzfeTiWg6EH8gsGf3g_500a03b1b95f41518a73c1368c767cf1_egg_production.csv

---

### 🗺️ State Lookup

https://d3c33hcgiwev3.cloudfront.net/19-hx8-BR_-X1DPaV5IPvw_13da3a9d4c244bcb87a24f7367e492f1_state_lookup.csv

---

# 📌 Data Preparation

Before answering the business questions, the datasets were prepared through a series of preprocessing steps, including:

- **Data cleaning**
- **Formatting numeric values**
- **Removing non-numeric characters**
- **Data validation**
- **Database normalization**
- **Consistency checks**
- **Preparation for SQL aggregation and Machine Learning analysis**

These preprocessing steps ensured data integrity and improved the reliability of all subsequent SQL analyses and predictive models.
