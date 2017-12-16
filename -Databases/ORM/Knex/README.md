# Knex.js (SQL Query Builder Library)

## Pre-Requisites
This material should come after **RDBMS** and **promises** and before **ORM** and **Bookshelf**. Students should already be familiar with **dynamic database queries**, **expressjs** and **promises**.

## Class Format / Time to Allow for Subject 
This material usually takes .5 day(s) to introduce and 1 day(s) of exercises and reinforcement.  

# Topics & Expected Outcomes

#### Levels of Understanding
Students will have *one of three* levels of understanding about each topic upon completion of this module.  
- **grok**: fully understand the topic in order to replicate code, communicate, and explain concepts without referring to any notes.  
- **explain**: understand enough about the topic to describe concepts without referring to notes.  
- **know about**: understand enough to look up further documentation when asked about the subject.  

#### Knex
-  Students should **fully grok** where knex.js fits into back-end application process.
-  Students should **fully grok** writing querying tables with knex.raw SQL statemnts and built in methods. 
-  Students should be able to **explain** what a query builder is and the benefit of using them.
-  Students should be able to **explain** model schemas and schemas for varying data structures and business requirements.
-  Students should know about the concepts and capabilties of an ORM
    - Migrations
    - Seeding
    - Models
    - Associations

# Suggested Format For Delivery
The following format is meant to be a guideline for effective delivery. Instructors can present material in another way if it is more effective for the students.  

1. Introduce 
1. Present **Intro to SQL**: [http://devleague.slides.com/devleague/intro-sql](http://devleague.slides.com/devleague/intro-sql)
1. Release **Knex.js + Node.js Setup** (Live-code?):
[https://gist.github.com/NigelEarle/80150ff1c50031e59b872baf0e474977](https://gist.github.com/NigelEarle/80150ff1c50031e59b872baf0e474977)
1. Release **Knex.js Migrations and Seeding** (Live-code?): 
[https://gist.github.com/NigelEarle/70db130cc040cc2868555b29a0278261](https://gist.github.com/NigelEarle/70db130cc040cc2868555b29a0278261)
1. Integrate knex.js into **Articles-Products-Express**:
[https://github.com/devleague/articles-products-and-express](https://github.com/devleague/articles-products-and-express) _(Using raw queries with `knex.raw()`)_
1. Exercise **Knex-Shopping**:
[https://github.com/devleague/knex-shopping](https://github.com/devleague/knex-shopping)(Using built in knex.js query methods)

# Slides & Examples

#### SQL
- Link: [http://devleague.slides.com/devleague/intro-sql](http://devleague.slides.com/devleague/intro-sql)
- Time Needed to Present: <= 30 minutes   
- Type: **Slideshow**

#### Knex Setup + Node
- Link: [https://gist.github.com/NigelEarle/80150ff1c50031e59b872baf0e474977](https://gist.github.com/NigelEarle/80150ff1c50031e59b872baf0e474977)
- Time Needed to Present: <= 1 hour
- Type: **Livecode**

#### Knex Migrations and Seeding
- Link: [https://gist.github.com/NigelEarle/70db130cc040cc2868555b29a0278261](https://gist.github.com/NigelEarle/70db130cc040cc2868555b29a0278261)
- Time Needed to Present: <= 1 hour
- Type: **Livecode**

# Exercises & Projects
The following exercises and projects state an average time alotted. A session is about 3 hours. There are 3 sessions in a day: (1) After the morning challenge up to lunch, (2) after lunch up to dinner, (3) after dinner until the end of class.


#### Articles-Products-Express
- Repository: [https://github.com/devleague/articles-products-and-express](https://github.com/devleague/articles-products-and-express)
- Average Time Alotted: 6 session
- Individual or Group Exercise: Individual
- Completed Example (Knex): [https://github.com/NigelEarle/articles-products-and-express/tree/knex-solutions](https://github.com/NigelEarle/articles-products-and-express/tree/knex-solutions)
- Concepts Practiced: **SQL**, **Knex.js**, **Dyanmic Database Queries**, **Express**, **Promises**
- Notes: Integrate Knex.js into existing DB layer of exercises.

#### Knex-shopping
- Repository: [https://github.com/devleague/knex-shopping](https://github.com/devleague/knex-shopping)
- Average Time Alotted: 6 sessions
- Individual or group: Individual
- Completed Example: [https://github.com/NigelEarle/knex-shopping/tree/solution](https://github.com/NigelEarle/knex-shopping/tree/solution)
- Concepts Practiced:  **SQL**, **Knex.js**, **Dyanmic Database Queries**, **Express**, **Promises**

# Additional Resources

#### Knex Documentation
- Link: [Knex Documentation](http://knexjs.org/)  
- Concepts: Knex usage/api reference
- Notes: Knex documentation

#### Knex Express PG YouTube Tutorial
- Link: [Knex + Express + PG YouTube Tutorial](https://www.youtube.com/watch?v=4nP6zFEvF_c&list=PL7sCSgsRZ-smPRSrim4bX5TQfRue1jKfw)  
- Concepts: Knex, Express, PG Usage
- Notes: Knex, Express, PG tutorial project, CRUD actions utilizing dynamic DB inserts, updates and queries.