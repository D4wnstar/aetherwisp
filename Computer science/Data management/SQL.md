---
wiki-publish: true
---
The **Structured Query Language** is the standard [[domain-specific language]] used to query a [[Relational model|relational]] [[database management system]].
## Introduction to SQL
As SQL is designed for data manipulation, the most important keywords to be aware of are `CREATE`, `DROP` and `ALTER`. In order, these are the general keywords used to create, delete and modify metadata in the DB. They almost always appear in some capacity when writing to the DB itself, typically followed by another keyword to specify the object that is being written to.

> [!tip] Casing
> SQL is not case-sensitive. This means that `create`, `drop` and `alter` are also correct, as is any other casing. This is true both for keywords and non-keywords: casing is only relevant in strings. By convention, it is considered standard to write keywords in uppercase to make them stand out from non-keyword elements of the query, and [[casing conventions|snake_case]] is considered the standard casing style for non-keywords.

Creation of [[database]] is handled with `CREATE DATABASE <name>`, where `<name>` is the name of the DB. Within the database, a table is created with `CREATE TABLE <name>`, followed by the schema of the table in parentheses. Here's an example:

```sql
CREATE TABLE students (
	id INTEGER PRIMARY KEY,
	name TEXT NOT NULL,
	surname TEXT NOT NULL,
	date_of_birth DATE NOT NULL,
	phone VARCHAR(13)
);
```

This query creates a table called `students` that contains an `id`, a `name`, a `surname`, a `date_of_birth` and a `phone` number.

The **primary key** is a special attribute that determines how each element (**row**) in the table is supposed to be identified. It has special semantics. A primary key:
- Must always be defined (`NOT NULL`).
- Must be `UNIQUE`.
- Implicitly defines an **index** (see below).

`NOT NULL` and `UNIQUE` are somewhat self-explanatory: the former disallows having an "empty" (`NULL`) cell in the row, while the latter disallows repeated values across different rows. A primary key is not mandatory. You can create a table with no primary key, although in general it is best to always have a primary key unless you have a specific reason why you shouldn't have one.[^1] Let's see another table:

```sql
CREATE TABLE exams (
	course VARCHAR(20),
	grade INTEGER NOT NULL CHECK grade >= 0 AND grade <= 10,
	honors BOOLEAN NOT NULL,
	date DATE NOT NULL DEFAULT CURRENT DATE,
	student_id INTEGER,
	CONSTRAINT honors_cons CHECK grade = 10 OR honors = FALSE,
	CONSTRAINT fk_1 FOREIGN KEY (student_id) REFERENCES students(id) ON DELETE CASCADE ON UPDATE CASCADE
);
```

This table introduces many new things. The `grade` columns has a **check**, specifically an **atomic check**. A check is used to determine if a row can or cannot be inserted into the table by defining a **constraint**. For example, trying to insert an exam with a negative grade or a grade above 10 would cause an error and not change the database. `CHECK` statements allow enforcing custom properties that the values in the column should always follow. The general syntax of a check is

```sql
CHECK [column] [op] [constant]
```

where `[column]` is the name of a column, `[op]` is a check operator and `[constant]` is some constant value used for the check. Some check operators are:
- `=`: equality.
- `<>`: inverse of `=`, non-equality.
- `<`: less than.
- `<=`: less than or equal to.
- `>`: greater than.
- `>=`: greater than or equal to.

In this table we also see a **logical connective**: `AND`. Logical connectives are used to set multiple checks on the same column: here we require that values in the `grade` column must be non-negative AND less than or equal to 10. The logical connectives are `AND`, `OR` and `NOT`, with the usual meaning. `AND` and `OR` must be placed between checks, like `CHECK [check1] AND [check2]`. Meanwhile, `NOT` goes before a check, like `CHECK NOT [check]`. Note that you only write `CHECK` once, at the start, even if you string multiple checks together.

The kind of check seen here is called a **domain constraint**. A domain constraint depends only on exactly one attribute of one row (`grade`, in this case). Notably, it could've also been written in a simpler way. The SQL standard includes a bespoke keyword for this kind of domain constraint: `BETWEEN`. This keyword is used to check if a numerical value is, well, between two values. The `grade` column can be defined more succinctly as `grade INTEGER BETWEEN 0 AND 10`.

There are other types of constraint, in increasing degree of complexity. **Tuple constraints** depend on multiple attributes, but still on a single row. This includes the constraint at the bottom of the table definition above. **Intrarelation constraints** depend on one or more attributes across different rows. These include `UNIQUE` and `PRIMARY KEY`, which must check if a value exists in a different row. Finally, **interrelation constraints** depend on one or more attributes, across different rows, and across different *tables*. These are the most complex constraints and also the most computationally expensive.

Constraints can also be defined manually with the `CONSTRAINT` keyword. In this table, we define a constraint called `honors_cons` that requires all rows to either have a `grade` of 10 or no honors. This encodes the idea that honors can only be given on an exam with the highest grade, so there should never be a row that has honors without a 10/10 grade.

Next up, we see that columns can have a `DEFAULT` value. When inserting a new row, you can omit specifying the value for these columns: if you do, the row will use the default value. In this case, if you add a new exam, you can omit specifying the date. If you do, it will use the `CURRENT DATE`, which is a special internal function of the DBMS that fetches the current date. More commonly, you'll use a constant. The syntax is `DEFAULT [value]` where value is a constant or a special value like `CURRENT DATE`.

Finally, look at the second constraint. We define a **foreign key**. Foreign keys are quite possibly the most foundational element of a relational database, because they define the *relations*. A foreign key is a value (here an `INTEGER`) that `REFERENCES` a value in a *different* table (here, the `id` of the `students` table). This relation allows formalizing the relations in the data: an exam can only recorded if there is a student that took it. No student, no exam. Then, through this foreign key, we can jump between tables. If we want to know more about the student that took an exam, we can use the foreign key to look the student up in the `students` table. Viceversa, we can find all exams by a student by filtering for the student's ID in the `exams` table.

Despite being the lifeblood of relational databases, adding a foreign key introduces all sorts of complexities. Most importantly, we now need to think about **foreign key integrity**. This refers to the synchronization of the key across both tables. If the foreign key and the original key fall out of sync, the system breaks. Therefore, we need to be *very* careful about any key that has foreign references, on *all* the tables that share that reference (here `students` and `exams`). More concretely, we need to make sure that all changes of these keys occur in lockstep across all tables that reference that key. Here's a practical example: say a student is removed from the database (maybe they're expelled). What happens to the exams they took? Well, the student ID is now deleted, so the `student_id` column in the `exams` table would be broken: some rows point to a student that doesn't exist anymore! These broken references are called **dangling references**[^2] and are, by default, disallowed. If you try to delete a row that is referenced somewhere by a foreign key, the DBMS will refuse and give you an error complaining about "constraint violations". In order to delete a row that is being reference, you first need to delete *everything* that is referencing that row, then the row itself.
## Retrieving data
When it comes to retrieving data from a table, SQL performs two basic operations: **projection** and **selection**. Projection refers to retrieving a subset of columns from a table. Selection instead refers to retrieving a subset of rows. In simple terms, they refer to filtering columns and rows respectively. The two can be (and often are) done simultaneously in order to filter both at the same time. Take the following query:

```sql
SELECT name, surname FROM students;
```

This query is a projection of the `student` table, filtering for just the `name` and `surname` columns. So selection is requested, so all rows are returned. The result is the names of surnames of all students in the table.

Projection, in SQL, is simply done by listing the columns you want after `SELECT`. You may opt out of projection by requesting all columns using the `*` wildcard:[^3]

```sql
SELECT * FROM students; -- Returns all columns and rows from students
```

Selection on the other hand is done in a variety of ways. Unlike projection, selection is opt-in: no selection is done by default. One basic way of selecting is by adding a special keyword after `SELECT`. For example, the `DISTINCT` keyword returns only rows that are different from each other (*all* selected fields must be the same for two rows to not be considered distinct):

```sql
SELECT DISTINCT name, surname from student;
```

This selects only students with distinct name/surname pairs. Students with the same name or surname are fine, but not both. You may notice that the `SELECT` keyword matches the term "selection". In fact, all `SELECT` queries technically run a selection, but the default is to allow everything through unless otherwise asked. You can make this explicit by adding the `ALL` selection keyword: it does nothing, because it's the default behavior, but it is allowed.

```sql
SELECT ALL name, surname from student; -- Same result as without ALL
```

The uses of `DISTINCT` are somewhat limited, however, in part because it's computationally expensive. Meanwhile, `ALL` is redundant. As such, this way of selecting is simple, but not that useful. In practice, selection is generally done through the much more powerful `WHERE` keyword. `WHERE` takes one or more conditions that are checked against the value of each row. If a row passes the conditions, then it's returned. Otherwise, it's ignored. Let's see an example:

```sql
SELECT name, surname
FROM students
WHERE YEAR(date_of_birth) = 2000 AND name LIKE "M%";
```

This query introduces a couple new features. Firstly, we see that `WHERE` conditions are related by a logical connective, just like constraints. Further, the `YEAR` builtin function extracts the year out of a `DATE` object. We then check that it is equal to 2000. The syntax is otherwise essentially the same as constraints: if you think about it, a `WHERE` clause *is* a constraint, only checked during retrieval instead of insertion. We also see another new keyword: `LIKE`. This keyword is one of many ways to run checks on strings. Specifically, it checks that the string matches the pattern placed after it.[^5] This pattern says "any string that starts with M".

A `WHERE` check returns an optional boolean value, meaning it can return "true", "false" or "undefined". The last one occurs when the check is done against a `NULL` value (and the check does not look for a null value). For example, if `date_of_birth` were nullable, the check `YEAR(date_of_birth) = 2000` would be undefined whenever `date_of_birth` would be `NULL`. In practice, "undefined" checks are equivalent to "false" checks: they are discarded all the same.
### Aliasing
When selecting from a table in SQL, you generally request the column names directly, such as `SELECT name FROM student`. However, this is actually [[syntax sugar]]: strictly speaking, you are supposed to explicitly write out the name of the table before each column to let SQL know where the column is:

```sql
SELECT students.name FROM students;
```

The table and column names are divided by a period character, like `<table>.<column>`. This might seem redundant and, in this case, it absolutely is. SQL is smart enough to know that if you request a single table, it should take all columns from that table, so you can safely omit it. However, specifying table ownership becomes relevant when you select from multiple tables through *joins*, where multiple tables might have columns with the same name.

It is possible to rename tables and columns on the fly for the purpose of the query only. This is called **aliasing** and it is useful in two main cases: for brevity when specifying table names explicitly, or to rename columns in the output. Aliasing is done with the `AS` keyword, like so:

```sql
SELECT S.name, S.surname FROM students AS S;
```

Here we are renaming `students` to `S` so that referring to it in the query is shorter.[^4] Columns can also be renamed:

```sql
SELECT S.name as A, S.surname as B FROM students AS S
```

This query is the same as before, but the requested columns in the output will be called `A` and `B` instead of `name` and `surname`.
### Sorting
Sorting is done through the `ORDER BY` keywords. These take one or more keys to sort by, specified as column names, and the ordering to use, specified using the `ASC` or `DESC` keywords (for ascending and descending order). For example:

```sql
SELECT surname, name
FROM students
ORDER BY surname ASC, name ASC;
```

This returns the names and surnames of all students in (ascending) alphabetical order. For students with the same surname, the names are also ordered in (ascending) alphabetical order.
### Combining tables
The purpose of a relational database is to formalize the relationships between entities. Once defined, these allow you to later retrieve data from multiple different tables based on their relationships. This is known as **joining** tables. While joining might be the most characteristic way of combining tables in SQL, it isn't the only way. It is possible to query for multiple tables without invoking relations and combine their items: this is called a **product** of the tables. Let's see how this works in practice.

The simplest table combination is a **[[Cartesian product]]**. This combines all the columns and all the rows from two tables in a single, much larger table. For example, take these two tables, $\text{T1}$ and $\text{T2}$.

| A   | B   | C   |
| --- | --- | --- |
| a   | b   | c   |
| 0   | 0   | 0   |
| a   | 0   | c   |

| D   | F   |
| --- | --- |
| d   | e   |
| 0   | e   |


The Cartesian product of the two, $\text{T}_{C}=\text{T1}\times\text{T2}$, is

| A   | B   | C   | D   | F   |
| --- | --- | --- | --- | --- |
| a   | b   | c   | d   | e   |
| a   | b   | c   | 0   | e   |
| 0   | 0   | 0   | d   | e   |
| 0   | 0   | 0   | 0   | e   |
| a   | 0   | c   | d   | e   |
| a   | 0   | c   | 0   | e   |

The product contains all combinations of rows and columns from both tables. The number of rows and columns is simply the product of the individual tables:
$$N_\text{rows}=N_\text{rows,T1}\cdot N_\text{rows,T2},\qquad N_\text{cols}=N_\text{cols,T1}\cdot N_\text{cols,T2}$$
## Manipulating data
Retrieving data is a reading operation. You see existing data in some form. The data, of course, must also be written somehow. This section deals with the three main data manipulation operations in SQL: `INSERT`, `DELETE` and `UPDATE`.

`INSERT` allows adding either new data or computed data to the database. New data is simplest to introduce: to add new data to a table, just use `INSERT INTO` with

```sql
INSERT INTO <table_name> [(<list_attributes>)]
VALUES (val_1, ..., val_k)[, (val_1, ..., val_k), ...]
```

Here square brackets indicate optional elements. Let's unpack this. `INSERT INTO` is the keyword, followed by the name of the table to insert into. Then, optionally, the attributes (column) to insert into. If omitted, it assumes you are adding a value to all columns in the order the table is defined with (meaning, a full row). This is useful when some columns are nullable or have default values and you want to keep the defaults. Then, after the `VALUES` keyword, a list of tuples. Each tuple is one row and you can optionally insert multiple rows at the same time. Here's an example:

```sql
INSERT INTO students
VALUES (123, 'John', 'Johnson', DATE('2000/04/11'), '3918219932'),
       (124, 'Jane', 'Dawson', DATE('1999/01/02'), NULL);
```

Here we are adding two new rows to the `students` table. Since we are not specifying the attribute list, SQL expects us to specify every column, in precisely in the order we used when defining the table. We could have also did:

```sql
INSERT INTO students (id, name, surname, date_of_birth)
VALUES (123, 'John', 'Johnson', DATE('2000/04/11')),
       (124, 'Jane', 'Dawson', DATE('1999/01/02'));
```

This is the same as before, expect we are explicitly listing the attributes. Note that `phone` is missing here: it's a nullable column, so it'll just default to `NULL` in both rows.

Let's talk about computed data now. As an example, let's define a new table:

```sql
CREATE TABLE summary (
	id INTEGER PRIMARY KEY,
	name TEXT NOT NULL,
	surname TEXT NOT NULL,
	num_exams INTEGER NOT NULL,
	avg_grade INTEGER
);
```

This table will contain some metadata about each student, namely the number of completed exams and the average grade. We'll calculate this metadata from existing data in the database like this:

```sql
INSERT INTO summary
AS (SELECT S.id, S.name, S.surname, COUNT(E.student_id), AVG(E.grade)
	FROM students as S LEFT OUTER JOIN exams as E
	ON E.student_id = S.id
	GROUP BY S.id, S.name, S.surname
);
```

There's a quite a bit going on here. `INSERT INTO summary` is similar to before, but now we are using `AS` instead of `VALUES`. This is how we tell SQL that we need to compute the data instead of inserting new constants. Then, in parenthesis, instead of a tuple of values we put a *query*. Here we use a `SELECT`, where we retrieve the appropriate ID/name/surname from the `students` table, then do some computation (`COUNT` and `AVG`)  on the `exams` table by joining the two by the student ID. We then group everything by ID/name/surname for clarity.

Computed value insertions take arbitrary queries, as long as their return the correct schema, so they can be come quite elaborate.

That's all for the basics of data insertion. To do the opposite, deleting data, we use the `DELETE` keyword:

```sql
DELETE FROM <table_name> [WHERE <condition>]
```

Deleting is much simpler. It simply deletes any row that matches the given condition. If no condition is given, all the contents of the table will be deleted. Remember that deleting is permanent and there's no coming back, so be careful! For example, to delete all students named "John":

```sql
DELETE FROM students WHERE name = 'John';
```

Finally, you might want to modify existing rows. This is done through the `UPDATE` keyword:

```sql
UPDATE <table_name>
SET <attribute> = <expression>
[WHERE <condition>]
```

The syntax is very similar to `DELETE`, except you also have a `SET` statement to tell SQL what columns to update. For example, to remove the phone number from all students named "Jane":

```sql
UPDATE students
SET phone = NULL
WHERE name = 'Jane';
```

## Automation
Maintaining the internal consistency of a database requires automating some operations that must always happen as a consequence of others actions. The standard way of doing this is to use a **trigger**. A trigger is an automated database operation that occurs as a reaction to an event (the operation is "triggered"). The event is a data manipulation operation: `INSERT`, `UPDATE` or `DELETE`. They are primarily meant to enforce consistency.

A trigger is defined with `CREATE TRIGGER`. For example:

```sql
CREATE TRIGGER update_student_name
	BEFORE INSERT
	ON students
	FOR EACH ROW
	EXECUTE FUNCTION update_student_name();
```

Here we are creating a new trigger called `update_student_name`. It triggers every time (specifically *before*) something is inserted in the `students` table, and when it does, it executes the function `update_student_name()` for each newly inserted row. A **function** is a collection of one or more operations organized in a single reusable block; for more on functions, see below. We also see a new concept: trigger timing. When we define a trigger condition (here, insertion on `students`), we get to choose whether the triggered operation (the function) happens `BEFORE` or `AFTER` the condition. In this case we choose `BEFORE`; for example, `update_student_name()` might standardize the formatting of the name to keep data consistent *before* inserting it into the database. `AFTER` would've executed the function after insertion. Furthermore, the `FOR EACH ROW` line is optional. If omitted, the trigger is ran once when the condition is met, instead of once per modified row.

Trigger functions are very powerful tools in SQL, though they can be a bit complicated to get into at first. The fact of the matter is that you can't write functions in SQL itself: the language is just meant to interface with the database, not write arbitrary functions. You have to use a different programming language. In the field, these are called **procedural languages** (usually prefixed with "pl") and, many times, existing standard languages like Python can be adapted to work in this context. Other times, bespoke languages are created for this very purpose: for example, PostgreSQL provides the `plpgsql` language for function definitions. This article uses `plpgsql` for function definitions. Since function definitions in SQL can be quite different from what you might expect coming from other languages, let's just see an example first:

```sql
CREATE FUNCTION update_student_name()
	RETURNS trigger
	LANGUAGE 'plpgsql'
AS $BODY$
BEGIN
	New."name" := UPPER(New."name");
	New."surname" := UPPER(New."surname");
	RETURN New;
END;
$BODY$;
```

This query is made of two parts. First, we have the SQL part. The function is made with `CREATE FUNCTION` followed by the name and the properties of the function. We tell SQL it's a trigger function written in `plpgsql`. Then, we start the `$BODY$` of the function: after this keyword we start writing the second part, which is the actual function body in the language of your choice (here `plpgsql`). We won't go into detail about `plpgqsql` syntax itself, but what this body does is that it takes the newly inserted row, automatically provided to the function as the `New` variable, then overwrites the `name` and `surname` cells with uppercase versions of themselves using the `UPPER()` function and the `:=` assignment operator. Finally, it returns the modified row `New`. This function, when paired with the previous trigger, guarantees that all names and surnames in the `students` table are uppercase by running this function before any insertion.

Let's see another example with a different use case. Recall the `summary` table from the [[#Manipulating data]] section. Every time a new student enrolls in the university, we need a new summary entry for them. This *can* be done manually, but why? It must happen every time, with precisely the same behavior. This is a perfect moment to use a trigger. Let's make a trigger to automatically add a new row to `summary` whenever a new student enrolls.

```sql
CREATE FUNCTION init_summary()
	RETURNS trigger
	LANGUAGE 'plpgsql'
AS $BODY$
BEGIN
	INSERT INTO summary
	VALUES (New."name", New."surname", 0, NULL);
END;
$BODY$;

CREATE TRIGGER init_summary
	AFTER INSERT
	ON students
	FOR EACH ROW
	EXECUTE FUNCTION init_summary();
```

Great, now every time a student is inserted into the `students` table, a new entry is added to `summary` with their name, surname and the default values for exam count and average grade. Now each student is guaranteed to have an associated summary for them. But we're not done. We need to also keep the summary up to date whenever the student passes an exam. To do so, we'll make another trigger that runs on insertion to `exams`.

```sql
CREATE FUNCTION update_summary()
	RETURNS trigger
	LANGUAGE 'plpgsql'
AS $BODY$
BEGIN
	UPDATE summary AS S
	SET New."num_exams" := New."num_exams" + 1,
		New."avg_grade" := AVG(
			SELECT grade FROM exams as E
			WHERE E."student_id" = New."student_id";
		)
	WHERE S."id" = New."student_id";
END;
$BODY$;

CREATE TRIGGER update_summary
	AFTER INSERT
	ON exams
	FOR EACH ROW
	EXECUTE FUNCTION update_summary();
```

Here the trigger simply increases the exam count by one each time an exam is passed and recalculates the average. To recalculate it, we select all existing exams for the given student within the trigger itself. Notably, this is *not* a good way of doing this. It's expensive and leads to a lot of unnecessary `SELECT` queries, but it is easy to read for an educational example.

[^1]: A table with no primary key has no guarantee that two rows are different, so you can have two identical rows with no way to distinguish them. Further, there is no automatic index definition. This may or may not be desired behavior. Also, what happens in the background is not defined and depends on the DBMS in use. For example, PostgreSQL and SQLite internally generate a unique identifier for each row even if you don't add a primary key. However, you cannot reference it and it's meant for internal use.

[^2]: In reference to dangling pointers from the C language, which are conceptually very similar. A foreign key is basically a pointer to a column value. If you know pointers, you can probably tell why foreign keys are hard.

[^3]: You can also manually list all the columns if you want. It's generally unnecessary, but it does allow you to specify the order in which the columns are returned, if that ever matters.

[^4]: Like before, explicit table naming is technically unnecessary here. It's just to make an example.

[^5]: It's not a [[regular expression]], but the idea is basically the same.
