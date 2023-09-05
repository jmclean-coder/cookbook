# Queries with Aggregates Pt. 1

SQL also supports the use of aggregate expressions and functionsthat allow us to summarize information about a group of rows of data.

```SQL
-- Select query with aggregate functions over all rows

SELECT AGG_FUNC(column_or_expression) AS aggregate_description, …
FROM mytable
WHERE constraint_expression;
```

Without specified group, an aggregate function will run on the whole set of result rows and return a single value. Like normal expressions, giving my aggregate function an alias ensure that the results will be easier to read and process.

## Common Aggregate Functions

| Function | Description |
| -------- | ----------- |
| COUNT(*), COUNT(column)| A common function used to count the number of rows in the group in the group, if no column name is specified. Otherwise, count the number of rows in the group with non-NULL values in the specified column. |
| MIN(column) | Finds the smallest numerical value in the specified column for all rows in the group. | 
| MAX(column) | Finds the largest numerical value in the specified column for all rows in the group. |
| AVG(column) | Finds the average numerical value in the specified column for all rows in the group. |
| SUM(column) | Finds the sum of all numerical values in the specified column for the rows in the group. |

## Grouped Aggregate functions

In addition to aggregating across all the rows, we can instead apply the aggregate function to individual groups of data within that group (ie. sales of action games compared to horror games)

This creates as many result rows as there are unique groups defined by the GROUP BY clause.

```SQL
--Select query with aggregate functions over groups

SELECT AGG_FUNC(column_or_expression) AS aggregate_description, …
FROM mytable
WHERE constraint_expression
GROUP BY column;
```

The `GROUP BY` clause works by grouping rows that have the same value in the column specified.

