# **__Capstone Project – Acting as a Data Scientist at the USDA__**

In this Capstone Project, I assume the role of a Data Scientist at the`USDA (United States Department of Agriculture)`. My responsibility is to <ins>analyze agricultural production data</ins> and <ins>provide insights that support decision-making</ins> across multiple departments.

The USDA maintains several datasets, including milk production, cheese production, coffee production, honey production, yogurt production, and a state reference table containing state names and ANSI codes. Using <ins>SQL</ins>, I answer business questions from managers and stakeholders by <ins>extracting, analyzing, prediction and interpreting data</ins>.

Throughout this project, I received the following requests:

> 1. Calculate the total milk production for 2023 to support the USDA annual report. And make predictions for three years after the last one

> 2. Identify the states whose cheese production exceeded 100 million pounds in April 2023 so that the Cheese Department could focus its marketing efforts on those regions.

> 3. Analyze coffee production trends and determine the total coffee production for the year 2011. and make predictions for three years after the last one

> 4. Calculate the average honey production for 2022 in preparation for a meeting with the Honey Council. And make a predition for the year 2023 and 2030.

> 5. Generate a list of all states and their corresponding ANSI codes for the State Relations Team.

> 6. Create a cross-commodity report listing all states and their cheese production values, including states that did not report cheese production in April 2023, and determine the production value for New Jersey.

> 7. Calculate the total yogurt production in 2022 for states that also had cheese production data available in 2023 to support planning by the Dairy Division.

> 8. Identify all states present in the state_lookup table that were missing from the milk_production dataset in 2023 in order to detect gaps or inconsistencies in reporting.

> 9. Produce a complete list of states and their cheese production values, including states with no reported production, and verify whether Delaware produced any cheese in April 2023.

> 10. Determine the average coffee production for all years in which honey production exceeded one million units, supporting comparative analysis between agricultural commodities.

<ins>To complete these requests:</ins>, I used SQL techniques including filtering with WHERE clauses, aggregate functions such as SUM and AVG, GROUP BY operations, subqueries, and JOINs. These analyses allowed me to transform raw agricultural data into actionable insights that support reporting, strategic planning, and operational decision-making within the USDA.

This project simulates <ins>real-world Data Science responsibilities</ins>, where business stakeholders frequently request specific analyses and expect accurate, data-driven answers to support organizational goals.

<ins>Through these analyses, I supported decision-making processes by transforming raw agricultural data into actionable insights. The project strengthened my ability to work with relational databases, write complex SQL queries, perform data validation, identify trends and anomalies, make predictions and communicate results to business stakeholders. This experience reflects the day-to-day responsibilities of a Data Scientist working with real-world agricultural production data at the USDA.</ins>

## *Query 1* 

```
</SQL>

SELECT Year,
       Sum(Value) AS Total
FROM Milk
GROUP BY Year
ORDER BY Year DESC
```      

```
</SQL>

Output:

|  Nº | Year |  Total |
| --: | ---: | -----: |
|   1 | 1924 |  12365 |
|   2 | 1925 |  12480 |
|   3 | 1926 |  10804 |
|   4 | 1927 |   8996 |
|   5 | 1928 |   9059 |
|   6 | 1929 |   9294 |
|   7 | 1930 |  50614 |
|   8 | 1931 |  58030 |
|   9 | 1932 |  70432 |
|  10 | 1933 |  77335 |
|  11 | 1934 |  75579 |
|  12 | 1935 |  80844 |
|  13 | 1936 |  83476 |
|  14 | 1937 |  83543 |
|  15 | 1938 |  86743 |
|  16 | 1939 |  87336 |
|  17 | 1940 |  88008 |
|  18 | 1941 |  89418 |
|  19 | 1942 |  90987 |
|  20 | 1943 |  89397 |
|  21 | 1944 |  91308 |
|  22 | 1945 |  90460 |
|  23 | 1946 |  89411 |
|  24 | 1947 |  90774 |
|  25 | 1948 |  89047 |
|  26 | 1949 |  89859 |
|  27 | 1950 |  91323 |
|  28 | 1951 |  89493 |
|  29 | 1952 |  86977 |
|  30 | 1953 |  90090 |
|  31 | 1954 |  91438 |
|  32 | 1955 |  90987 |
|  33 | 1956 |  91030 |
|  34 | 1957 |  90238 |
|  35 | 1958 |  86550 |
|  36 | 1959 |  87721 |
|  37 | 1960 | 110313 |
|  38 | 1961 | 111613 |
|  39 | 1962 | 111320 |
|  40 | 1963 | 111065 |
|  41 | 1964 | 109648 |
|  42 | 1965 | 105320 |
|  43 | 1966 | 107197 |
|  44 | 1967 | 106698 |
|  45 | 1968 | 106030 |
|  46 | 1969 | 108082 |
|  47 | 1970 | 108557 |
|  48 | 1971 | 108812 |
|  49 | 1972 | 106199 |
|  50 | 1973 | 101345 |
|  51 | 1974 | 102068 |
|  52 | 1975 | 100984 |
|  53 | 1976 |  99189 |
|  54 | 1977 |  97842 |
|  55 | 1978 |  98552 |
|  56 | 1979 |  94005 |
|  57 | 1980 |  93831 |
|  58 | 1981 |  96939 |
|  59 | 1982 |  31910 |
|  60 | 1983 |  95293 |
|  61 | 1984 |  94834 |
|  62 | 1985 |  96597 |
|  63 | 1986 |  81173 |
|  64 | 1987 |  85124 |
|  65 | 1988 |  84203 |
|  66 | 1989 |  84087 |
|  67 | 1990 |  87310 |
|  68 | 1991 |  85901 |
|  69 | 1992 |  88779 |
|  70 | 1993 |  88105 |
|  71 | 1994 |  89072 |
|  72 | 1995 |  89273 |
|  73 | 1996 |  88420 |
|  74 | 1997 |  88773 |
|  75 | 1998 |  87609 |
|  76 | 1999 |  85366 |
|  77 | 2000 |  87685 |
|  78 | 2001 |  91021 |
|  79 | 2002 |  86855 |
|  80 | 2003 |  96391 |
|  81 | 2004 | 101478 |
|  82 | 2005 |  98435 |
|  83 | 2006 | 103410 |
|  84 | 2007 | 101837 |
|  85 | 2008 |  99156 |
|  86 | 2009 |  97248 |
|  87 | 2010 |  96510 |
|  88 | 2011 |  99272 |
|  89 | 2012 |  99325 |
|  90 | 2013 | 101979 |
|  91 | 2014 | 103396 |
|  92 | 2015 | 105149 |
|  93 | 2016 | 107163 |
|  94 | 2017 | 103320 |
|  95 | 2018 | 101320 |
|  96 | 2019 | 100435 |
|  97 | 2020 | 102613 |
|  98 | 2021 |  95890 |
|  99 | 2022 | 100845 |
| 100 | 2023 |  35947 |

```

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

```

```
</>Python

total = pd.read_csv ('year_total_milk.csv')

```

```
</>Python

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

```
</>Python

list(total.columns)

```

```
</>Python

Output:

['Year', 'Total']

```

```
</>Python

dados = total

print(dados)

```

```
</>Python

Output:

| No. | Year |  Total |
| --: | ---: | -----: |
|   1 | 1924 |  12365 |
|   2 | 1925 |  12480 |
|   3 | 1926 |  10804 |
|   4 | 1927 |   8996 |
|   5 | 1928 |   9059 |
|   ⋮ |    ⋮ |      ⋮ |
|  96 | 2019 | 100435 |
|  97 | 2020 | 102613 |
|  98 | 2021 |  95890 |
|  99 | 2022 | 100845 |
| 100 | 2023 |  35947 |

```

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

<img width="983" height="590" alt="image" src="https://github.com/user-attachments/assets/1a598961-a094-4f0d-a00a-0c855d293c96" />

##  *Query 2*

```
</SQL>

SELECT st.State,
       v.Value,
       Period
FROM Cheese v
     LEFT JOIN State st ON v.State_ANSI = st.State_ANSI
WHERE Value > 100000000 AND
      Year = "2023" AND
      Period = "APR"

```

```
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

```

##  *Query 3*


```
</SQL>

SELECT Year,
       Sum(Value) AS Total
FROM coffee
GROUP BY Year

```

```
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

```

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

```

```
</>Python

total = pd.read_csv ('year_total_coffe.csv')

```

```
</>Python

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

```
</>Python
list(total.columns)
```

```
</>Python

Output:
['Year', 'Total']

```

```
</>Python

dados = total

print(dados)

```

```
</>Python

Output:

| No. | Year | Total |
| --: | ---: | ----: |
|   1 | 1946 |     8 |
|   2 | 1947 |     8 |
|   3 | 1948 |     7 |
|   4 | 1949 |     5 |
|   5 | 1950 |     9 |
|   6 | 1951 |     9 |
|   7 | 1952 |    10 |
|   8 | 1953 |    10 |
|   9 | 1954 |    12 |
|  10 | 1955 |    10 |
|  11 | 1956 |    11 |
|  12 | 1957 |    18 |
|  13 | 1958 |    10 |
|  14 | 1959 |    12 |
|  15 | 1960 |    13 |
|  16 | 1961 |     8 |
|  17 | 1962 |    13 |
|  18 | 1963 |     6 |
|  19 | 1964 |     9 |
|  20 | 1965 |     7 |
|  21 | 1966 |     8 |
|  22 | 1967 |     5 |
|  23 | 1968 |     5 |
|  24 | 1969 |     4 |
|  25 | 1970 |     4 |
|  26 | 1971 |     2 |
|  27 | 1972 |     3 |
|  28 | 1973 |     3 |
|  29 | 1974 |     1 |
|  30 | 1975 |     1 |
|  31 | 1976 |     2 |
|  32 | 1977 |     2 |
|  33 | 1978 |     1 |
|  34 | 1979 |     2 |
|  35 | 1980 |     1 |
|  36 | 1981 |     2 |
|  37 | 1982 |    10 |
|  38 | 1983 |     2 |
|  39 | 1984 |     1 |
|  40 | 1985 |     1 |
|  41 | 1986 |     3 |
|  42 | 1987 |     1 |
|  43 | 1988 |     2 |
|  44 | 1989 |     3 |
|  45 | 1990 |     2 |
|  46 | 1991 |     2 |
|  47 | 1992 |     2 |
|  48 | 1993 |     2 |
|  49 | 1994 |     4 |
|  50 | 1995 |     5 |
|  51 | 1996 |     6 |
|  52 | 1997 |     9 |
|  53 | 1998 |     9 |
|  54 | 1999 |    10 |
|  55 | 2000 |     8 |
|  56 | 2001 |     8 |
|  57 | 2002 |     7 |
|  58 | 2003 |     8 |
|  59 | 2004 |     5 |

```

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

```
</>Python

Output:

```

<img width="881" height="595" alt="image" src="https://github.com/user-attachments/assets/ae0bb803-24c4-4f1b-a548-0f55519e45d3" />

##  *Query 4* 

```
</SQL>

SELECT Year,
       ROUND(AVG(Value), 2) AS Average
FROM honey
GROUP BY Year

```

```
</SQL>

Output:

| Nº | Year | Average |
| -: | ---: | ------: |
|  1 | 1987 |  143.43 |
|  2 | 1988 |  108.45 |
|  3 | 1989 |  176.67 |
|  4 | 1990 |  146.16 |
|  5 | 1991 |  144.09 |
|  6 | 1992 |  145.76 |
|  7 | 1993 |  209.27 |
|  8 | 1994 |  202.33 |
|  9 | 1995 |  171.82 |
| 10 | 1996 |  191.24 |
| 11 | 1997 |  168.07 |
| 12 | 1998 |  181.14 |
| 13 | 1999 |  184.18 |
| 14 | 2000 |  193.55 |
| 15 | 2001 |  198.44 |
| 16 | 2002 |  223.80 |
| 17 | 2003 |  183.64 |
| 18 | 2004 |  187.50 |
| 19 | 2005 |  197.86 |
| 20 | 2006 |  217.71 |
| 21 | 2007 |  212.83 |
| 22 | 2008 |  204.48 |
| 23 | 2009 |  202.66 |
| 24 | 2010 |  176.51 |
| 25 | 2011 |  180.02 |
| 26 | 2012 |  182.80 |
| 27 | 2013 |  136.70 |
| 28 | 2014 |  216.80 |
| 29 | 2015 |  177.73 |
| 30 | 2016 |  179.88 |
| 31 | 2017 |  133.95 |
| 32 | 2018 |  165.49 |
| 33 | 2019 |  185.83 |
| 34 | 2020 |  226.68 |
| 35 | 2021 |  175.56 |
| 36 | 2022 |  140.25 |

```

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

```

```
</>Python

average = pd.read_csv ('Year,Average.csv')

```

```
</>Python

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

```
</>Python

list(average.columns)

```

```
</>Python

['Year', 'Average']

```

```
</>Python

dados = average

print(dados)

```

```
</>Python

Outpút:

| No. | Year | Average |
| --: | ---: | ------: |
|   1 | 1987 |  143.43 |
|   2 | 1988 |  108.45 |
|   3 | 1989 |  176.67 |
|   4 | 1990 |  146.16 |
|   5 | 1991 |  144.09 |
|   6 | 1992 |  145.76 |
|   7 | 1993 |  209.27 |
|   8 | 1994 |  202.33 |
|   9 | 1995 |  171.82 |
|  10 | 1996 |  191.24 |
|  11 | 1997 |  168.07 |
|  12 | 1998 |  181.14 |
|  13 | 1999 |  184.18 |
|  14 | 2000 |  193.55 |
|  15 | 2001 |  198.44 |
|  16 | 2002 |  223.80 |
|  17 | 2003 |  183.64 |
|  18 | 2004 |  187.50 |
|  19 | 2005 |  197.86 |
|  20 | 2006 |  217.71 |
|  21 | 2007 |  212.83 |
|  22 | 2008 |  204.48 |
|  23 | 2009 |  202.66 |
|  24 | 2010 |  176.51 |
|  25 | 2011 |  180.02 |
|  26 | 2012 |  182.80 |
|  27 | 2013 |  136.70 |
|  28 | 2014 |  216.80 |
|  29 | 2015 |  177.73 |
|  30 | 2016 |  179.88 |
|  31 | 2017 |  133.95 |
|  32 | 2018 |  165.49 |
|  33 | 2019 |  185.83 |
|  34 | 2020 |  226.68 |
|  35 | 2021 |  175.56 |
|  36 | 2022 |  140.25 |

```

```
</>Python

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

```
</>Python

Output:

```



## *Query 5*

```
</SQL>

SELECT *
FROM State

```

```
</SQL>

Output:

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

```

## *Query 6*

```
</SQL>

SELECT st.State,
       v.Value,
       Period
FROM Cheese v
     LEFT JOIN State st ON v.State_ANSI = st.State_ANSI
WHERE Year = "2023" AND
      Period = "APR"

```

```
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

```

## *Query 7*

```
</SQL>

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

```
</SQL>

Output:

Aqui está a tabela organizada:

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

```

## *Query 8*

```
</SQL>

SELECT sl.state,
       (
           SELECT (Count(State) - 26)
           FROM State
       ) AS States_That_Do_Not_Have_Records_2023_MILK
FROM state sl
     LEFT JOIN milk mp ON sl.state_ansi = mp.state_ansi AND
                          mp.year = 2023
WHERE mp.state_ansi IS NULL

```

```
</SQL>

Output:

| Nº | State          | States_That_Do_Not_Have_Records_2023_MILK |
| -: | -------------- | ----------------------------------------: |
|  1 | ALABAMA        |                                        24 |
|  2 | ALASKA         |                                        24 |
|  3 | ARKANSAS       |                                        24 |
|  4 | CONNECTICUT    |                                        24 |
|  5 | DELAWARE       |                                        24 |
|  6 | HAWAII         |                                        24 |
|  7 | KENTUCKY       |                                        24 |
|  8 | LOUISIANA      |                                        24 |
|  9 | MAINE          |                                        24 |
| 10 | MARYLAND       |                                        24 |
| 11 | MASSACHUSETTS  |                                        24 |
| 12 | MISSISSIPPI    |                                        24 |
| 13 | MISSOURI       |                                        24 |
| 14 | MONTANA        |                                        24 |
| 15 | NEBRASKA       |                                        24 |
| 16 | NEVADA         |                                        24 |
| 17 | NEW HAMPSHIRE  |                                        24 |
| 18 | NEW JERSEY     |                                        24 |
| 19 | NORTH CAROLINA |                                        24 |
| 20 | NORTH DAKOTA   |                                        24 |
| 21 | OKLAHOMA       |                                        24 |
| 22 | RHODE ISLAND   |                                        24 |
| 23 | SOUTH CAROLINA |                                        24 |
| 24 | TENNESSEE      |                                        24 |
| 25 | WEST VIRGINIA  |                                        24 |
|  2 | WYOMING        |                                        24 |


```

## *Query 9*

```
</SQL>

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
           WHEN Year = '2023' AND
                Period = 'APR' THEN 'Valid'
           ELSE 'Invalid'
       END Valitor
FROM Cheese v
     LEFT JOIN State st ON v.State_ANSI = st.State_ANSI
GROUP BY State

```

```
</SQL>

Output:

| Nº | State         |       Value | Period | Year | Validator |
| -: | ------------- | ----------: | :----: | ---: | :-------- |
|  1 | NULL          | 215,206,000 |   APR  | 2023 | Valid     |
|  2 | ALABAMA       |   2,118,000 |  NULL  | NULL | Invalid   |
|  3 | ARKANSAS      |  23,166,000 |  NULL  | NULL | Invalid   |
|  4 | CALIFORNIA    | 208,807,000 |   APR  | 2023 | Valid     |
|  5 | COLORADO      |   3,550,000 |   APR  | NULL | Invalid   |
|  6 | CONNECTICUT   |   5,213,000 |  NULL  | NULL | Invalid   |
|  7 | IDAHO         |  86,452,000 |   APR  | 2023 | Valid     |
|  8 | ILLINOIS      |   5,068,000 |   APR  | 2023 | Valid     |
|  9 | INDIANA       |  27,183,000 |  NULL  | NULL | Invalid   |
| 10 | IOWA          |  31,512,000 |   APR  | 2023 | Valid     |
| 11 | KANSAS        |   2,937,000 |   APR  | NULL | Invalid   |
| 12 | KENTUCKY      |   3,135,000 |   APR  | NULL | Invalid   |
| 13 | LOUISIANA     |   6,325,000 |  NULL  | NULL | Invalid   |
| 14 | MASSACHUSETTS |      93,000 |   APR  | NULL | Invalid   |
| 15 | MICHIGAN      |   8,835,000 |   APR  | NULL | Invalid   |
| 16 | MINNESOTA     |  69,728,000 |   APR  | 2023 | Valid     |
| 17 | MISSISSIPPI   |     874,000 |   APR  | NULL | Invalid   |
| 18 | MISSOURI      |   8,645,000 |   APR  | NULL | Invalid   |
| 19 | MONTANA       |   1,844,000 |  NULL  | NULL | Invalid   |

```

## *Query 10*

```
</SQL>

SELECT AVG(c.value) AS avg_coffee_production
FROM coffee c
     JOIN honey h ON c.year = h.year
WHERE h.value > 1000000

```

```
</SQL>

Output:

  avg_coffee_production
1 5.87062404870624

```

## *Function to Update The DataBase*

<img width="940" height="460" alt="Function_to_Update_DataBase" src="https://github.com/user-attachments/assets/205ce7cd-bf80-4cae-b47a-c80b37744326" />

+ I used this function to remove commas to perform calculations from the database.

## *DataBase*

https://d3c33hcgiwev3.cloudfront.net/d8zmGGSKQ5-IF7c4DXBz6Q_60a7f48eface44f59708149f249585f1_cheese_production.csv?Expires=1781305762&Signature=Ju-ikVdEF8k870d47EmwO7PxpTM1dalcxVFAqVJOHBpLSow6JkqQLpAb8PNiSW1ZpUBAbzMuWTvm3xO4Rjeu1mI0M5p4a6L8R~v1vK6XVqlqDvjnZHTj42tedFrFAE0q8KFitN3~5JqKPAdxeNKDj7LIM0WgwDvRJvDqgr6m0KM_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A
https://d3c33hcgiwev3.cloudfront.net/X-LJUUv5SuyuwXCNIG7wGQ_31442ea85cab45858dc0881c6e15dbf1_honey_production.csv?Expires=1781305762&Signature=ccyYbfLX9~ZSBQKqTCEHXQ8m35UHknivqHnt7FhOmAO3aZwq0sWj5fYzgbI4RnUDUXYaYfiEr4jnek9My99c4rhtuuu7BL9iCX~uEps8OgM95Bv8ZOz7n4a7nPIvpfzQUHjlcUDKX6O8h4FVJNq1OuYZsSkGGq-m7KLTGp~J6Og_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A
https://d3c33hcgiwev3.cloudfront.net/hqFfV_kBR8ikF2T4p-X9Iw_3c34b5199b614bb19e7d56936872dff1_milk_production.csv?Expires=1781305762&Signature=EglXI32xcLzlUIoNbBGKMPeifFaddOErXnq~bWnntmhljt9NBN~q1~GwhWUnSqM98CeFMc4T5i6Fc5afkve8-ly0dAp0QTX3GGfv8gUEOPnw0IED9E~7LALcfcUV70AzA0H9FD~rflmyjTHfATIdnlc4AiA-1W9NmgtZHPoImv8_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A
https://d3c33hcgiwev3.cloudfront.net/B7_yyiTsRnCz1j19KE-_xA_4c4db332472344238d67147334902df1_coffee_production.csv?Expires=1781305762&Signature=jlrGGeZErNIv132VA6cafsf9vn8hkvfuhA~438rjys4bEMZ9eI-Dc2rrNTgLDPlE4y6SZloebjQi3Xu1WwSbRvk3KjBdpA2lhjtlEjnVVAydmAOylI-vA6HorxpolzGcnGSHxEjGOBAYknrIdJMkemQ5HI89Y3ROcVV6~KriSZc_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A
https://d3c33hcgiwev3.cloudfront.net/DXHlHzfeTiWg6EH8gsGf3g_500a03b1b95f41518a73c1368c767cf1_egg_production.csv?Expires=1781305762&Signature=aNaGlxuACZ~9bw969yuMyInRHhMFIC5IZPFh~Miti1uDFUTUCye2Tz6v5Wg2r9m2ETmKF3oSYxmGCCUR0B0axB9MNqh~32~lsemOp0jRukXzeQj1L8myI7VlCDaxMpVm55zgyaAIFTC709xll0KvRfcQOr9PVREItLZqBG7-m9w_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A
https://d3c33hcgiwev3.cloudfront.net/19-hx8-BR_-X1DPaV5IPvw_13da3a9d4c244bcb87a24f7367e492f1_state_lookup.csv?Expires=1781305762&Signature=fDFvwOOLsZkD75~JXChTkH~HhtjamCOflZQ7YXI4yLvDoieuHMVLmAWu~1rwyQ32~TFR4~VUuxLO0XEfq4BcaI~GWtyN8Ew7OJo~1wc4hCFGrTRiGaAESF0n9f79NVNXnXn8v1T0t54ov2~~TOEtQZUs8~G8TcJsoiLt17UOBVw_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A
https://d3c33hcgiwev3.cloudfront.net/2oDLa7X0QnCuYmqLFs5bbg_4124f56804084ec884ef97089ed52ef1_yogurt_production.csv?Expires=1781305762&Signature=HLmOMfsmi08gVp111Jf0z8HtDR4QZa8AhvrYKeAwPC3a1bZ6eA71d9z-o1hD~aWiExpz5d6ftS2wx8bRYrBM2LEcerd-fvCkFpfLjCUYB9G0NKmhOZbRBbDMYehQ7AoJ4RiPsnVMgra6x6VNZghK5CA3rRgXh5o6KXZwrrkPinw_&Key-Pair-Id=APKAJLTNE6QMUY6HBC5A
