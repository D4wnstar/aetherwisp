---
wiki-publish: true
---
The **Structured Query Language** is the standard [[domain-specific language]] used to query a [[Relational model|relational]] [[database management system]].
## Introduction to syntax
As SQL is designed for data manipulation, the most important keywords to be aware of are `CREATE`, `DROP` and `ALTER`. In order, these are the general keywords used to create, delete and modify either data or metadata in the DB. They almost always appear in some capacity when writing to the DB, typically followed by another keyword to specify the object that is being written to.

One note: SQL is not case-sensitive. This means that `create`, `drop` and `alter` are also correct, as is any other casing. This is true both for keywords and non-keywords: casing is only relevant in strings. By convention, it is considered standard to write keywords in uppercase to make them stand out from non-keyword elements of the query.

Creation of [[database]] is handled with `CREATE DATABASE <name>`, where `<name>` is the name of the DB. Within the database, a table is created with `CREATE TABLE <name>`, followed by the schema of the table in parentheses. Here's an example:

```sql
CREATE TABLE students (
	id INTEGER PRIMARY KEY,
	name TEXT NOT NULL,
	surname TEXT NOT NULL,
	phone VARCHAR(13)
)
```

This query creates a table called `students` that contains an `id`, a `name`, a `surname` and a `phone` number.

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

[^1]: A table with no primary key has no guarantee that two rows are different, so you can have two identical rows with no way to distinguish them. Further, there is no automatic index definition. This may or may not be desired behavior. Also, what happens in the background is not defined and depends on the DBMS in use. For example, PostgreSQL and SQLite internally generate a unique identifier for each row even if you don't add a primary key. However, you cannot reference it and it's meant for internal use.

[^2]: In reference to dangling pointers from the C language, which are conceptually very similar. A foreign key is basically a pointer to a column value. If you know pointers, you can probably tell why foreign keys are hard.
