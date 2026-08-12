# Order By
The ORDER BY clause in SQL sorts a query's result set in ascending (ASC, default) or descending (DESC) order based on one or more specified columns.

## Syntax
```sql
SELECT *
FROM Table
ORDER BY Score (either ASC or DESC)
```

## Problem

```sql
/* Retrieve all customers and 
   sort the results by the highest score first. */
SELECT *
FROM customers
ORDER BY score DESC
```

| id | first_name | country | score |
| :- | :--------- | :------ | :---- |
| 2  | John       | USA     | 900   |
| 3  | Georg      | UK      | 750   |
| 4  | Martin     | Germany | 500   |
| 1  | Maria      | Germany | 350   |
| 5  | Peter      | USA     | 0     |

```sql
/* Retrieve all customers and 
   sort the results by the lowest score first. */
SELECT *
FROM customers
ORDER BY score ASC
```

|**id**|**first_name**|**country**|**score**|
|---|---|---|---|
|5|Peter|USA|0|
|1|Maria|Germany|350|
|4|Martin|Germany|500|
|3|Georg|UK|750|
|2|John|USA|900|

```sql
/* Retrieve all customers and 
   sort the results by the country. */
SELECT *
FROM customers
ORDER BY country ASC
```

|**id**|**first_name**|**country**|**score**|
|---|---|---|---|
|1|Maria|Germany|350|
|4|Martin|Germany|500|
|3|Georg|UK|750|
|5|Peter|USA|0|
|2|John|USA|900|

```sql
/* Retrieve all customers and 
   sort the results by the country and then by the highest score. */
SELECT *
FROM customers
ORDER BY country ASC, score DESC
```

|**id**|**first_name**|**country**|**score**|
|---|---|---|---|
|4|Martin|Germany|500|
|1|Maria|Germany|350|
|3|Georg|UK|750|
|2|John|USA|900|
|5|Peter|USA|0|

```sql
/* Retrieve the name, country, and score of customers 
   whose score is not equal to 0
   and sort the results by the highest score first. */
SELECT
    first_name,
    country,
    score
FROM customers
WHERE score != 0
ORDER BY score DESC
```

|**first_name**|**country**|**score**|
|---|---|---|
|John|USA|900|
|Georg|UK|750|
|Martin|Germany|500|
|Maria|Germany|350|

---

[Previous Page : Where Clause](./Where%20Clause.md) | [Next Page : Group By](./Group%20By.md) | [Return To Index](../README.md)
