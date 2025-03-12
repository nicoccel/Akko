# Mirror x SQL SERVER

INTERWORLD

Wiki x sql server

## Stored Procedures

[DOC](https://www.sqlservertutorial.net/sql-server-stored-procedures/basic-sql-server-stored-procedures/)

It's a set of SQL instructions that are executed sequentially within a database.
It's a block of code that can be called multiple times by different applications or users, without having to rewrite the code every time.

### Benefits of Stored Procedures

- Optimize performance, reducing network traffic and database workload
- Simplify data management, providing a unified interface for accessing and modifying data

### Using Stored Procedures

- Execute complex queries that require managing data from multiple tables.
- Update data atomically, ensuring data consistency.
- Perform calculations and generate reports efficiently.
- Manage data access permissions and authorizations.

#### What is Atomicity on database ?

[DOC](https://en.wikipedia.org/wiki/Atomicity_(database_systems))

### Return value

[DOC](https://learn.microsoft.com/it-it/sql/t-sql/functions/error-number-transact-sql)

## Function

[DOC](https://learn.microsoft.com/en-us/sql/t-sql/statements/create-function-transact-sql)

### Scalar Valued

Return a single value.

### Table Valued

Return rows of data

## Function vs Stored Procedures

[DOC](https://stackoverflow.com/a/1179778)

## Schema

[DOC](https://www.sqlservertutorial.net/sql-server-basics/sql-server-create-schema/)

Default SCHEMA is `dbo`

- Organization: Schemas help organize database objects, such as tables, views, and stored procedures, into logical groups. This makes it easier to manage and maintain the database.
- Security: Schemas can be used to implement security at a more granular level. You can grant permissions to specific schemas, rather than to the entire database, which helps to limit access to sensitive data.
- Namespace management: Schemas help to avoid naming conflicts between objects in different parts of the database. By using a schema, you can have multiple objects with the same name, as long as they are in different schemas.
- Data separation: Schemas can be used to separate data into different logical groups, such as separating data for different applications or departments.
- Easier database migration: Schemas can make it easier to migrate databases between different environments, such as from development to production.
- Improved performance: In some cases, using schemas can improve query performance by reducing the number of objects that need to be searched.

## Variable

It is possible to use variables in stored procedures, passing them as input. These variables can be used, initialized with the `@` symbol followed by the name and then AS with the data type. All of this is enclosed in parentheses after the name of the stored procedure.
If a variable is followed by `OUTPUT`, it means that it will be a return value.

Example of a global variable : `DECLARE @name VARCHAR(2)`

Fixed values ​​can be assigned to variables `SET @variable = 1;`
Such as assigning them from the results of the queries `SELECT @variabile = column FROM table WHERE condition;`

### Type

- `IDENTITY(1,1)` x auto-increment

## Table

### Temporary tables

[DOC](https://stackoverflow.com/a/2219731)

For create it use `CREATE TABLE #TempTable (ID INT,Nome NVARCHAR(50),Età INT);`
For delete it use `DROP TABLE #TempTable;`

## Index

[DOC](https://www.sqlservertutorial.net/sql-server-indexes/)

### Clustered

[DOC](https://learn.microsoft.com/en-us/sql/relational-databases/indexes/create-clustered-indexes)

### Nonclustered

[DOC](https://learn.microsoft.com/en-us/sql/relational-databases/indexes/create-nonclustered-indexes)

### Fill Factor

[DOC](https://learn.microsoft.com/en-us/sql/relational-databases/indexes/specify-fill-factor-for-an-index)

`... WITH FILLFACTOR = n`
It is common to use the primary filegroup, since these tables exist only for the duration of the session and are automatically eliminated when they are no longer necessary.
`ON [PRIMARY]`

## Clauses

All clauses

### Offset Fetch

[DOC](https://www.sqlservertutorial.net/sql-server-basics/sql-server-offset-fetch/)

### Top

[DOC](https://learn.microsoft.com/en-us/sql/t-sql/queries/top-transact-sql)

The `TOP` command is general for everyone, the subtles are for SQL Server

#### Top N Percent

`N` is the percentage of lines that must be returned.

#### With Ties

The records returned, (eg) of the specified columns, which have the same values ​​as the selected values.

## Select

- Is it possible to do a `SELECT` without `FROM`.
    This command can serve to make more sets of values ​​to the variables all together.
- If the education is performed on a fixed value, the value in tabular format will be returned.
- If it is performed to set multiple variables (multiple `SET`) nothing will be returned, you can use `@@ROWCOUNT` to check that the operation has been successful (the value must be 1).
- It is possible to use `SELECT` for choose the variables to be used as values ​​in an `INSERT INTO`

## Trigger

[OFFICIAL](https://learn.microsoft.com/en-us/sql/t-sql/statements/create-trigger-transact-sql?view=sql-server-ver16)
[DOC](https://www.sqlservertutorial.net/sql-server-triggers/)

## Commands Legend

- `SET NOCOUNT ON` x disable the return of the number of modified lines
- `BEGIN TRANSACTION` x start
- `COMMIT TRANSACTION` x end ok
- `ROLLBACK TRANSACTION` x cancel all the changes made and restore the values ​​before the transaction [DOC](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/rollback-transaction-transact-sql)
- `SET ANSI_NULLS ON` x [DOC](https://stackoverflow.com/a/9766756)
- `SET QUOTED_IDENTIFIER ON` x [DOC](https://stackoverflow.com/a/45865446)
- `GO` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/sql-server-utilities-statements-go?view=sql-server-ver16&redirectedfrom=MSDN)
- `ALTER PROCEDURE [name_schema].[name_store_procedures]` x [DOC](https://stackoverflow.com/a/69726539)
- `AS` x if preceded by the initiation of an store procedures indicates the content of it, otherwise if preceded by the name of a column and followed by another name indicates a nickname of the column
- `RAISERROR` x [DOC](https://stackoverflow.com/a/16170114)
- `BEGIN` and `END` x [DOC](https://stackoverflow.com/a/404052)
- `CONVERT(type, value)` x [DOC](https://www.w3schools.com/SQL/func_sqlserver_convert.asp)
- `CONCAT(string1, string2, ...)` x [DOC](https://www.w3schools.com/SQL/func_sqlserver_concat.asp)
- `CASE` x [SEMPLE](https://www.w3schools.com/sql/sql_case.asp) or [OFFICIAL](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/case-transact-sql). They can be used to return a value to a variable based on conditions
- `EXECUTE` x [DOC ?](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/execute-transact-sql)
- `TRY CATCH`  x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/try-catch-transact-sql)
- `WAITFOR DELAY` x [DOC](https://stackoverflow.com/a/7676272)
- `WHILE (condition)` x [SQL](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/while-transact-sql)
- `USE [name_db]` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/language-elements/use-transact-sql)
- `<>` x [DOC](https://stackoverflow.com/a/7892)

## Function Legend

- `AVG()` x [DOC](https://www.w3schools.com/sql/sql_avg.asp)
- `LEFT(string, n)` x [DOC](https://www.w3schools.com/Sql/func_sqlserver_left.asp)
- `ISNULL(x, y)` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/functions/isnull-transact-sql)
- `ERROR_MESSAGE()` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/functions/error-message-transact-sql)
- `ERROR_SEVERITY()` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/functions/error-severity-transact-sql)
- `ERROR_STATE()` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/functions/error-state-transact-sql)
- `ERROR_NUMBER()` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/functions/error-number-transact-sql)

## Statment Legend

- `@@ROWCOUNT` x [DOC](https://stackoverflow.com/a/14474517) or [OFFICIAL](https://learn.microsoft.com/en-us/sql/t-sql/functions/rowcount-transact-sql)
- `@@SERVICENAME` x [DOC](https://learn.microsoft.com/en-us/sql/t-sql/functions/servicename-transact-sql)
