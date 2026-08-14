# Distinct

Removes Duplicates (Repeated Values)
DISTINCT removes duplicate rows from the result set. It’s used with SELECT to return only unique values (based on the columns you select).

## Syntax
```sql
SELECT DISTINCT
  Country
FROM Table
```
## Problem

```sql
-- Return Unique list of all countries
SELECT DISTINCT country
FROM customers
```
| country |
|---|
| Germany |
| UK |
| USA |

---

[Previous Page : Having Clause](./Where%20Clause.md) | [Next Page : ](./Top.md) | [Return to Index](../README.md)
