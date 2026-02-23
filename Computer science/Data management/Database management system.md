---
wiki-publish: true
aliases:
  - DBMS
---
A **database management system** (**DBMS**) is a software system meant to manage and operate on [[database|databases]], usually considered alongside the data itself. They handle interrelated data by providing all the tools required to read and write the data in a structured, reliable, convenient and efficient manner. The basic operation done with a DBMS is called a **query**. For example, reading some data, appending new data, deleting existing data and joining related data from different sources are typical database queries.

Besides managing permanent storage, a common use case for a DBMS it to provide users with an abstract view of the data. This means deconstructing the original data to *view* it in a different way. The data itself is not changed, it is merely *seen* from a different perspective. This is, for example, useful to describe the content of the data, the relationships inside the data, or to abstract [[data structure|data structures]] to hide complexity.

Common [[SQL]] DBMSes include PostgreSQL, MySQL and SQLite.
## Introduction
In the early days, data management systems were built directly on top of the regular [[file system]] the [[operating system]] relies on. While technically easy (the file system is always present on a machine and its operation is guaranteed by the OS), this paradigm comes with several issues. Namely:
- Data is stored in many files with different formats, making it prone to data redundancy and duplication.
- Different file formats require many different implementations of serializers and deserializers, which is prone to bugs and technical debt.
- Constraints on data integrity (e.g., guaranteeing that a quantity is always greater than zero) become complicated to handle due to having to hand-code them every time. It also makes it difficult to add new constraints or remove existing ones.
- You are required to write a brand new program to access data. There's no centralized method of access (at least, not necessarily).
- Operations are not atomic, meaning that if an operations fails half-way through, it leaves the data in an inconsistent and probably corrupt state.
- Concurrency leaves a lot to be desired. It is necessary for performance, but relying on an external data model (the file system) makes it difficult to control how it is used.
- Security becomes difficult to enforce. File access controls (i.e., read/write/execute permissions) are provided by the file system, but this requires the DBMS to be totally reliant on OS administration, which is not in general reasonable. You cannot define database permissions separately from regular file permissions.

The solution? Just manage data separately from the regular file system! This way, all the pain points above becomes solvable, since the DBMS controls *everything*. Of course, this requires re-implementing the entire data access pipeline from scratch, but in a sense, that's precisely what we want. This idea is the foundation of all modern BDMSes.