# ORDER in SQL
## Coding Order

```sql
SELECT DISTINCT TOP 2
  col 1,
  SUM(col 2)
DROM Table
WHERE col = 1
HAVING SUM(col 2) > 30
ORDER BY col 1 ASC
```
- `SELECT` Filter Columns
- `DISTINCT ` Filters Duplicates
- `TOP ` Filter Result Rows
- `WHERE` Filter Rows Before Aggregation
- `HAVING ` Filter Rows After Aggregation

## Execution Order
▫1 `FROM`
▫2 `WHERE`
▫3 `GROUP BY`
▫4 `HAVING`
▫5 `SELECT DISTINCT`
▫6 `ORDER BY`
▫7 `TOP`

---

[Previous Page : Top](./Top.md) | [Next Page : ]() | [Return to Index](../README.md)
