# NULL Values

- It's a good, albeit noble, idea to reduce null values in SQL databases
    - The queries, constraints, and data processing are affected by null values.
    - Some functions handle null values differently
- One alternative to null is data-type appropriate default values, like 0 for integer, or an empty string for string.
    - If the database needs to store incomplete values, null values are a good option that won't skew data. example: an avrage would be skewed by zeros.
- sometimes it's impossible to avoid null values, like a case where two tables have asymmetric data.


## Testing for NULL Values

- We can test for NULL cvalues by using `NULL` or `IS NOT NULL` in a `WHERE` clause.
```SQL
SELECT name, breed
FROM dogs
WHERE breed IS/IS NOT NULL
AND/OR condition(s)
...;
```



