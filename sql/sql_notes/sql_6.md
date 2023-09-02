# Multi-Table Queries and JOINS


## Database Normalization 

- Minimizes duplicate data in tables and allows for independent growth of data
- Queries become more complex and performance issues will arise because of large tables
    - What kinds of performance issues?
        - N+1 Queries
        - Full table scans
- Good queries are design to efficiently combine and extract only the necessary data

Multi-Table Queries with JOINS

### INNER JOIN

- A process that matches rows from the first table and the second table which have the same key
- This key is commonly an auto incrementing integer, but could be a STRING, HASHED value. 
- KEYS MUST be unique.
- The KEY can be specified with the ON constraint


```sql
SELECT name, breed_name
FROM pets
INNER JOIN dogs
    ON pets.id = dogs.id
WHERE condition(s)
```

