# Queries with expressions

## Expressions
- We can perform more complex logic on column values in a query with expressions, these can be mathematical, string functions, and basic arithmetic.

example: 
```SQL
SELECT name, price / 0.2 AS twenty_percent_discount_price
FROM inventory
WHERE price < 30
```

There are different kinds of kinds of relational and non-relational databases 
<!-- ADD LINKS TO DOCS -->
- MySQL
- PostgreSQL
- SQLite
- Microsoft SQL Server
- and more!

Each database has it's only rules for syntax, aliases, math, string, and date functions.

Using expressions can save time a post-processing of Data. The main goal of SQL is to access data as quickly as possible.

It's recommended to use a descriptive alias for the expression with the `AS` command to make the query easier to read.

```SQL
SELECT col_expression AS expr_description, …
FROM mytable;
```