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
