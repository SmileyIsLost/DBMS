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
## Problem
```sql
/* Find the average score for each country
   and return only those countries with an average score greater than 430 */
SELECT
    country,
    AVG(score) AS avg_score
FROM customers
GROUP BY country
HAVING AVG(score) > 430
```
| country | avg_score |
|---|---:|
| UK | 750 |
| USA | 450 |

```sql
/* Find the average score for each country
   considering only customers with a score not equal to 0
   and return only those countries with an average score greater than 430 */
SELECT
    country,
    AVG(score) AS avg_score
FROM customers
WHERE score != 0
GROUP BY country
HAVING AVG(score) > 430
```
| country | avg_score |
|---|---:|
| UK | 750 |
| USA | 900 |

---

[Previous Page : Group By](./Group%20By.md) | [Next Page : Distinct](./Distinct.md) | [Return to Index](../README.md)
