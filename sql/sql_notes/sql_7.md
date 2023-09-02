# OUTER JOINS

## INNER JOIN vs. OUTER JOIN

- Both are SQL JOINS used to combine data from two or more tables in a database.

### INNER JOIN 

- INNER JOIN returns only the MATCHING rows between two tables based on a specified join condition.
    - non-matching rows are discarded.
- Result set contains only the rows that satisfy the JOIN condition

Example:
<!-- Insert Code Example -->
Visual:
![Inner Join Venn Diagram, left circle is table 1, right circle is table two, with the overlapping portion of the circles shaded.](<media/Inner Join.webp>)

### OUTER JOIN
- Returns all the rows from one table and matching rows from another table based on a specified join condition.
    - If no matching rows in the second table, the result with contain NULL values, for all columns of the second table.
#### LEFT OUTER JOIN / LEFT JOIN
- Returns all rows from the LEFT table and matching rows from the right table
    - If no matching matching rows, result will contain NULL values for all columns of LEFT table

Example:
<!-- Insert Code Example -->
Visual
![Left Join Venn Diagram, left circle is table 1, right circle is table two, table one circle is shaded](media/left_join.webp)
#### RIGHT OUTER JOIN / RIGHT JOIN
 - Returns all rows from the right table and matching rows from the left table. 
        - If there are no matching rows in the left table, the result set will contain NULL values for all columns of the left table.

Example: 
<!-- Insert Code Example -->
Visual:
![Right Join Venn Diagram, right circle is table 1, left circle is table two, table 2 circle is shaded](media/right_join.webp)
#### FULL OUTER JOIN / FULL JOIN
- Returns all rows from both tables. 
        - If there are no matching rows in one of the tables, result set will contain NULL values for all columns of the non-matching table.

Example: 
<!-- Insert Code Example -->
Visual:
![Right Join Venn Diagram, right circle is table 1, left circle is table two, both circles are shaded](media/full_join.webp)
