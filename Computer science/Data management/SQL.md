---
wiki-publish: true
---
The **Structured Query Language** is the standard [[domain-specific language]] used to query a [[Relational model|relational]] [[database management system]].
## Syntax
As SQL is designed for data manipulation, the most important keywords to be aware of are `CREATE`, `DROP` and `ALTER`. In order, these are the general keywords used to create, delete and modify either data or metadata in the DB. They almost always appear in some capacity when writing to the DB, typically followed by another keyword to specify the object that is being written to.

One note: SQL keywords are not case-sensitive. This means that `create`, `drop` and `alter` are also correct. However, by convention, it is considered standard to write keywords in uppercase (like above) to make them stand out from non-keyword elements of the query.

Creation of [[database]] is handled with `CREATE DATABASE <name>`, where `<name>` is the name of the DB. Within the database, a table is created with `CREATE TABLE <name>`, followed by the schema of the table in parentheses. Here's an example:

```sql
CREATE TABLE student (
	id INT PRIMARY KEY,
	name TEXT NOT NULL,
	surname TEXT NOT NULL,
	phone VARCHAR(13) -- e.g. 3418108191 or +393418108191
)
```

This query creates a table called `student` that contains an `id`, a `name`, a `surname` and a `phone` number.