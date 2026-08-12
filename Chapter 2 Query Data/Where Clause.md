# Where Clause
A WHERE clause filters rows based on a condition (e.g., only customers from Germany or orders with sales > 10), so only matching records appear in the results.


```sql
-- Retrieve customers with a score not equal to 0
SELECT *
FROM customers
WHERE score != 0
```

| id | first_name | country | score |
|---:|---|---|---:|
| 1 | Maria | Germany | 350 |
| 2 | John | USA | 900 |
| 3 | Georg | UK | 750 |
| 4 | Martin | Germany | 500 |

```sql
-- Retrieve customers from Germany
SELECT *
FROM customers
WHERE country = 'Germany'
```

| id | first_name | country | score |
|---:|---|---|---:|
| 1 | Maria | Germany | 350 |
| 4 | Martin | Germany | 500 |

```sql
-- Retrieve the name and country of customers from Germany
SELECT
    first_name,
    country
FROM customers
WHERE country = 'Germany'
```

| first_name | country |
| ---------- | ------- |
| Maria      | Germany |
| Martin     | Germany |

```sql
-- Retrieve all customers with a score greater than 500
SELECT *
FROM customers
WHERE score > 500
```
| id | first_name | country | score |
|---:|------------|----------|------:|
| 2 | John | USA | 900 |
| 3 | Georg | UK | 750 |


```sql
-- Retrieve all customers with a score  500 or more
SELECT *
FROM customers
WHERE score >= 500
```

| id | first_name | country | score |
|---:|------------|----------|------:|
| 2 | John | USA | 900 |
| 3 | Georg | UK | 750 |
| 4 | Martin | Germany | 500 |

```sql
-- Retrieve all customers with a score  less than 500
SELECT *
FROM customers
WHERE score < 500
```
| id | first_name | country | score |
|---:|------------|----------|------:|
| 1 | Maria | Germany | 350 |
| 5 | Peter | USA | 0 |

```sql

-- Retrieve all customers with a score  equal to or less than  500
SELECT *
FROM customers
WHERE score <= 500
```
| id | first_name | country | score |
|---:|------------|----------|------:|
| 1 | Maria | Germany | 350 |
| 4 | Martin | Germany | 500 |
| 5 | Peter | USA | 0 |

---
[Previous Page : Selecting Specific Columns](./Selecting%20Specific%20Columns.md) | [Next Page : Order By](./Order%20By.md) | [Return to Index](../README.md)
