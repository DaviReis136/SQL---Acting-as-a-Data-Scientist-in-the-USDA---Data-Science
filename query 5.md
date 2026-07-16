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
