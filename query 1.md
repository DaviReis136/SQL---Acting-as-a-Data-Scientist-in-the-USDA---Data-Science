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
