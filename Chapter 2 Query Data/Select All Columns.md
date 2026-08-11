# Select All Columns
Selecting all columns means using SELECT * to retrieve every field from a table

```sql
-- Retrieve All Customer Data
SELECT *
FROM customers
```

|  id | first_name | country | score |
| --: | ---------- | ------- | ----: |
|   1 | Maria      | Germany |   350 |
|   2 | John       | USA     |   900 |
|   3 | Georg      | UK      |   750 |
|   4 | Martin     | Germany |   500 |
|   5 | Peter      | USA     |     0 |

```sql
-- Retrieve All Order Data
SELECT *
FROM orders
```

| order_id | customer_id | order_date | sales |
| -------: | ----------: | ---------- | ----: |
|     1001 |           1 | 2021-01-11 |    35 |
|     1002 |           2 | 2021-04-05 |    15 |
|     1003 |           3 | 2021-06-18 |    20 |
|     1004 |           6 | 2021-08-31 |    10 |

---

[Previous Page : Comments](./Comments.md) | [Next Page : Selecting Specific Columns](./Selecting%20Specific%20Columns)
---
[Return to Index](../README.md)
