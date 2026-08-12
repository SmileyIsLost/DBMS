# Selecting Specific Columns
Selecting few columns means using `SELECT column1, column2` (instead of `SELECT *`) to return only the fields you need, which keeps results smaller and queries more focused.


## Problem
```sql
-- Retrieve each customer's name, country, and score.
SELECT 
    first_name,
    country, 
    score
FROM customers
```

| first_name | country | score |
| ---------- | ------- | ----: |
| Maria      | Germany |   350 |
| John       | USA     |   900 |
| Georg      | UK      |   750 |
| Martin     | Germany |   500 |
| Peter      | USA     |     0 |

---
## Practice
[Revising The Select Query I : Hacker Rank](https://www.hackerrank.com/challenges/revising-the-select-query/problem?isFullScreen=true)

---
[Previous Page : Select All Columns](./Select%20All%20Columns.md) | [Next Page : Operators](./Operators.md) | [Return To Index](../README.md)
