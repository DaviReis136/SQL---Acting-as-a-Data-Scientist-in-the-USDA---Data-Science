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
