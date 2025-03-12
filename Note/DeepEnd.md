# Deep End x SQL

INTERWORLD

Wiki x sql

## Type Variable

- `NULL` x
  - Indicates the absence of data or unknown information
  - Use the IS NULL operator to test if a value is NULL or not

## Clause

All types of clauses

### DISTINCT

The unique values ​​returns, if a value is repeated it will be returned only once.

### WHERE

...

### LIKE

[DOC](https://www.sqlservertutorial.net/sql-server-basics/sql-server-like/)

- `%` multiple characters
- `_` single character

#### IN

[DOC](https://www.w3schools.com/Sql/sql_in.asp)

#### BETWEEN

[DOC](https://www.w3schools.com/sql/sql_between.asp)

### GROUP BY

[DOC](https://www.w3schools.com/sql/sql_groupby.asp)

#### HAVING

[DOC](https://www.w3schools.com/sql/sql_having.asp)

### JOIN

[DOC](https://en.wikipedia.org/wiki/Join_(SQL))
[DOC](https://www.w3schools.com/sql/sql_join.asp)

`JOIN` and `INNER JOIN` [they have the same meaning](https://stackoverflow.com/a/565640)

#### INNER JOIN

Returns records that have matching values in both tables.
If there are no correspondences, you will not see any line in the result. Only lines with correspondences in both tables will be returned.
[DOC](https://www.w3schools.com/sql/sql_join_inner.asp)

#### LEFT JOIN

Returns all records from the left table, and the matched records from the right table.
You will see all the lines of the left table, even if there are no correspondences in the right table. In this case, the fields of the right table will be set to Null (or empty) for those lines of the left table that do not have correspondences.
[DOC](https://www.w3schools.com/sql/sql_join_left.asp)

#### RIGHT JOIN

Returns all records from the right table, and the matched records from the left table.
You will see all the lines of the right table, even if there are no correspondences in the left table. Here, the fields of the left table will be set to Null (or empty) for those lines of the right table that have no correspondences.
[DOC](https://www.w3schools.com/sql/sql_join_right.asp)

#### FULL JOIN

Returns all records when there is a match in either left or right table.
It is a combination of Left join and right join. Returns all the lines from both the United Tables, showing the results where there are correspondences.

- Correspondences: When there are lines that correspond in both tables, the results will be united, showing the data of both tables in a single line.
- No correspondence: if a row in one of the tables does not have a correspondence in the other table, the fields of the table without correspondence will be set to Null.

In this way, the full join allows you to view all the information available from both tables, even when there are no direct relationships between some lines.
[DOC](https://www.w3schools.com/sql/sql_join_full.asp)

## Statement

All type of tools

### Index

[DOC](https://stackoverflow.com/a/2955470)
[DOC](https://www.w3schools.com/sql/sql_create_index.asp)
[DOC](https://www.w3schools.com/SQL/sql_ref_index.asp)

## Help

- [DOC](https://stackoverflow.com/a/1629135) x `LIKE` on `DateTime` record
