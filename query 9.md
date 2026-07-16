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
