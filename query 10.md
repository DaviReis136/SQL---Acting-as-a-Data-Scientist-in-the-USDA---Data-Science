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
