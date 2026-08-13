# Group By
GROUP BY groups rows that have the same values in specified columns, and lets you apply aggregate functions like COUNT(), SUM(), AVG(), MIN(), MAX() per group.

## Problem

```sql
-- Find the total score for each country
SELECT 
    country,
    SUM(score) AS total_score
FROM customers
GROUP BY country
```
| country | total_score |
|---|---:|
| Germany | 850 |
| UK | 750 |
| USA | 900 |
- Here the `total_score` is an alias that only exist in this query and not in database
```sql
-- Find the total score and total number of customers for each country
SELECT 
    country,
    SUM(score) AS total_score,
    COUNT(id) AS total_customers
FROM customers
GROUP BY country
```
| country | total_score | total_customers |
|---|---:|---:|
| Germany | 850 | 2 |
| UK | 750 | 1 |
| USA | 900 | 2 |

### Group By rule
All columns in `SELECT` must be either aggregated or included in the `GROUP BY`
```sql
/* This will not work because 'first_name' is neither part of the GROUP BY 
   nor wrapped in an aggregate function. SQL doesn't know how to handle this column. */
SELECT 
    country,
    first_name,
    SUM(score) AS total_score
FROM customers
GROUP BY country
```
---

[Previous Page : Order By](./Order%20By.md) | [Next Page : Having Clause](./Having%20Clause.md) | [Return to Index](../README.md)
