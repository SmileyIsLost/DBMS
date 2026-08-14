# Top
It restrict the number of rows returned

## Syntax
```sql
SELECT TOP 3
*
FROM Table
```

## Problem

```sql
-- Retrieve only 3 Customers
SELECT TOP 3 *
FROM customers
```
| id | first_name | country | score |
|---:|------------|----------|------:|
| 1 | Maria | Germany | 350 |
| 2 | John | USA | 900 |
| 3 | Georg | UK | 750 |

```sql
-- Retrieve the Top 3 Customers with the Highest Scores
SELECT TOP 3 *
FROM customers
ORDER BY score DESC
```
| id | first_name | country | score |
|---:|------------|----------|------:|
| 2 | John | USA | 900 |
| 3 | Georg | UK | 750 |
| 4 | Martin | Germany | 500 |

```sql
-- Retrieve the Lowest 2 Customers based on the score
SELECT TOP 2 *
FROM customers
ORDER BY score ASC
```
| id | first_name | country | score |
|---:|------------|----------|------:|
| 5 | Peter | USA | 0 |
| 1 | Maria | Germany | 350 |

```sql
-- Get the Two Most Recent Orders
SELECT TOP 2 *
FROM orders
ORDER BY order_date DESC
```
| order_id | customer_id | order_date | sales |
|---------:|--------------:|:-----------|------:|
| 1004 | 6 | 2021-08-31 | 10 |
| 1003 | 3 | 2021-06-18 | 20 |

---

[Previous Page : Distinct](./Distinct.md) | [Next Page : Order in SQL](./Order-in-SQL.md) | [Return to Index](../README.md) 
