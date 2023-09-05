# Queries with aggregates (pt. 2)
What happens if the `GROUP BY` clause is executed after the `WHERE` clause? 
- `WHERE` filters the rows which are to be grouped, so how to be filter ALREADY grouped rows?

We use the `HAVING` clause!

`HAVING` is used specifically with either the `GROUP BY` clause to allow us to filter grouped rows from the result set.

```SQL
-- Select query with HAVING constraint
SELECT group_by_column, AGG_FUNC(column_expression) AS aggregate_result_alias, …
FROM mytable
WHERE condition
GROUP BY column
HAVING group_condition;
```

- `HAVING` clause contraints are written the same way as the `WHERE` clause constraints.
- They are applied to the grouped rows.
- This becomes more useful with millions of rows of different properties because we can apply additional constraints to quickly make sense of the data.
- If we aren;t using `GROUP BY` then there is no need for `HAVING`, and we can use `WHERE` instead.

