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
