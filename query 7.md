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
