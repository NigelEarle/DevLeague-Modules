# Relational DB Management System

## Pre-Requisites
This material should come after **server-side frameworks (express)** and before **ORM's** and **NoSQL**. Knowledge of **REPL** and **datatypes** is required for this subject.
## Class Format / Time Allowed For Subject
This material usually takes 1 day to introduce and 2.5 days of exercise and reinforcement.
## Topics & Expected Outcomes
#### Levels of Understanding
Students will have *one of three* levels of understanding about each topic upon completion of this module.  
- **grok**: fully understand the topic in order to replicate code, communicate, and explain concepts without referring to any notes.  
- **explain**: understand enough about the topic to describe concepts without referring to notes.  
- **know about**: understand enough to look up further documentation when asked about the subject. 

---

#### PostgreSQL
- Students should grok creating databases, users and tables
- Students should grok how to list users, databases, tables and columns of a table from the postgresql shell

#### SQL
- Students should grok SQL queries, inserts, update, join statements on tables
- Students should grok how to set datatypes of columns when creating tables
- Students should understand the benefits and disadvantages of indexing

#### Relationships
- Students should grok UML diagrams
- Students should understand normalizing database tables
    - 3 - 4 forms of database normalization
- Students should understand `one to one`, `one to many`, `many to many` and `many to one` relationships

# Suggested Format for Delivery
The following format is meant to be a guideline for effective delivery. Instructors can present material in another way if it is more effective for the students.

1. Introduce RDBMS; PostgreSQL
1. Present **SQL Slides**: [https://github.com/devleague/slides-sql](https://github.com/devleague/slides-sql)
1. Install **PostgreSQL**: [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
1. Assign **SELECT todo FROM list**: [https://github.com/devleague/SELECT-todo-FROM-list](https://github.com/devleague/SELECT-todo-FROM-list)
1. Assign **Automotive Index**: [https://github.com/devleague/Automotive-Index](https://github.com/devleague/Automotive-Index)
1. Introduce Database Normalization
    1. Whiteboard transferance of denormalized data to normalized
1. Assign **Denormal Automotives**: [https://github.com/devleague/Denormal-Automotives](https://github.com/devleague/Denormal-Automotives)
1. Whiteboard UML diagrams in small groups
1. Assign **Has Many Relationships**: [https://github.com/devleague/Has-Many-Relationships](https://github.com/devleague/Has-Many-Relationships)
1. Assign **SQL Blog Post** (morning exercise?): [https://gist.github.com/jaywon/80b3ceb78c2791c30950](https://gist.github.com/jaywon/80b3ceb78c2791c30950)
1. Check in on students, understanding of normalization, common SQL commands, UML diagrams
1. Introduce **Promises**
    1. Slide deck and Live Coding: [https://github.com/devleague/slides-promises](https://github.com/devleague/slides-promises)
1. Add **pg-promise** to **Articles,Products,Express Oh My!** repository [https://gist.github.com/JoeKarlsson1/495e9f002737e1693ddf](https://gist.github.com/JoeKarlsson1/495e9f002737e1693ddf)

# Slides & Examples

#### SQL
- Link: [https://github.com/devleague/slides-sql](https://github.com/devleague/slides-sql)
- Time needed to present: < 30 minutese
- Type: **Slideshow**
- Concepts Covered: *SQL*

#### Promises
- Link: [https://github.com/devleague/slides-promises](https://github.com/devleague/slides-promises)
- Time needed to present: < 30 minutes
- Type: **Slideshow**
- Concepts Covered: *Promises*

# Exercises & Projects
The following exercises and projects state an average time alotted. A session is about 3 hours. There are 3 sessions in a day: (1) After the morning challenge up to lunch, (2) after lunch up to dinner, (3) after dinner until the end of class.

#### SELECT-todo-FROM-list
- Repository: [https://github.com/devleague/SELECT-todo-FROM-list](https://github.com/devleague/SELECT-todo-FROM-list)
- Average Time Alotted: 2 sessions
- Individual or Group: Individual Exercise
- Completed Example: [#](https://google.com)
- Concepts Practiced: *PostgreSQL shell commands, Create database and user, Basic SQL queries -- select, insert, update, alter* 

#### Automotive-Index
- Repository: [https://github.com/devleague/Automotive-Index](https://github.com/devleague/Automotive-Index)
- Average Time Alotted: 2 sessions
- Individual or Group: Individual Exercise
- Completed Example: [#](https://google.com)
- Concepts Practiced: *Query large data sets, Indexing and performance*

#### Denormal-Automotive
- Repository: [https://github.com/devleague/Denormal-Automotives](https://github.com/devleague/Denormal-Automotives)
- Average Time Alotted: 2 sessions
- Individual or Group: Individual Exercise
- Completed Example: [#](https://google.com)
- Concepts Practiced: *Query large data sets, Normalizing datasets, JOIN statements*

#### Has-Many-Relationships
- Repository: [https://github.com/devleague/Has-Many-Relationships](https://github.com/devleague/Has-Many-Relationships)
- Average Time Alotted: 2 sessions
- Individual or Group: Individual Exercise
- Completed Example: [#](https://google.com)
- Concepts Practiced: *Relationships between tables(one-to-many, many-to-many etc.), Setting foriegn key on relational table, JOIN statements*

# Additional Resources

#### RDBMS
- Link: [https://en.wikipedia.org/wiki/Relational_database_management_system](https://en.wikipedia.org/wiki/Relational_database_management_system)
- Concepts: RDBMS history and explanation
- Notes: High level overview of RDBMS's

#### PostgreSQL
- Link: [https://www.postgresql.org/](https://www.postgresql.org/)
- Concepts: PostgreSQL home
- Notes: Postgres docs for version documentation, download links, about postgres, etc.

#### Normalization
- Link: [https://en.wikipedia.org/wiki/Database_normalization](https://en.wikipedia.org/wiki/Database_normalization)
- Concepts: Database normalization
- Notes: In depth look at database normalization. First, second and third normal form links included

#### JOIN Statements
- Link: [http://www.sql-join.com/](http://www.sql-join.com/)
- Concepts: SQL JOIN Statements
- Notes: Explanation of the different types of JOIN statements and how to use them
