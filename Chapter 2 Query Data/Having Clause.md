# Having
HAVING filters groups after GROUP BY is applied (so it works with aggregate results like SUM(score), COUNT(*), etc.).
It Filters Data after Aggregation

## Syntax
```sql
SELECT Country,
SUM(score)
FROM Table
GROUP BY Country
HAVING SUM(score)>800 (a condition)
```

