# ElasticSearch

## Pre-Requisites
This material should come after RDBMS/NoSQL and may come after or just before front end frameworks. Students should already be familiar with TDD/BDD, nodejs, express, and Revealing Module Pattern.

## Class Format / Time to Allow for Subject
This material usually takes 1 session to introduce and up to 2 sessions of exercises and reinforcement.

## Terms

- NoSQL
- Document
- Document Store
- Index / Indexing
- Type
- Query
- Term
- Mapping
- Shard
- Node

https://www.elastic.co/guide/en/elasticsearch/reference/current/glossary.html

## Querying and DSL
Docs for Query DSL docs can be found here: [https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html)
This is also listed as one of the resources in "Additional Resources".

Note: lucene syntax is supported in `q` queries.
https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-query-string-query.html

Simple Query String

https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-simple-query-string-query.html

## Topics & Expected Outcomes

#### Levels of Understanding
Students will have *one of three* levels of understanding about each topic upon completion of this module.

- **grok**: fully understand the topic in order to replicate code, communicate, and explain concepts without referring to any notes.

- **explain**: understand enough about the topic to describe concepts without referring to notes.

- **know about**: understand enough to look up further documentation when asked about the subject.

---

- Students should *be able to explain* installing and turning on an elasticsearch db
- Students should *be able to explain* creating an elasticsearch client
- Students should *know about* streaming logs, trace vs. error
- Students should *know about* using the elasticsarch server api with curl
- Students should *be able to explain* using the elasticsarch node client and library api
- Students should *be able to explain* creating a seed script
    - Students should be able to use npm scripts
    - Students should be able to write a separate utility in a separate subdirectory
    - Students should be able to document how to use the utility in the readme
    - Students should be able to explain data formatting, use Numbers (XXX @Jon is this said correctly?)
- Students should *be able to explain* and understand that in es, search size default is 10
- Students should *be able to explain* search query syntax
- Students should *be able to explain* how to get the source document from search result in js
- Students should *fully grok* the documentation [https://www.elastic.co/guide/en/elasticsearch/guide/current/document.html](https://www.elastic.co/guide/en/elasticsearch/guide/current/document.html)

# Suggested Format for Delivery
The following format is meant to be a guideline for effective delivery. Instructors can present material in another way if it is more effective for the students.

1. Walk through installing and running es server.
1. Walk through curl command to check that the es server is listening.
1. Walk through a basic node script to create a client that connects and pings the server.
1. Introduce utilities and helper libraries, though start with raw es. _do not use querybuilders at all during the exercise, just introduce it so that they may be used in future projects._
1. Students should practice lots of reading and navigating the well-written documentation.
1. Work on [Springy Findeon Exercise](https://github.com/devleague/Springy-Findeon)
1. Reminder: after students import the data, the server will take time (about a minute) to index the documents, so immediate queries may not include the new data.

# Exercises & Projects
The following exercises and projects state an average time alotted. A session is about 3 hours. There are 3 sessions in a day: (1) After the morning challenge up to lunch, (2) after lunch up to dinner, (3) after dinner until the end of class.

#### Springy Findeon
- Repository: [Springy Findeon Exercise](https://github.com/devleague/Springy-Findeon)
- Average Time Alotted: 2 sessions
- Completed Example: https://github.com/theRemix/Springy-Findeon
- Stretch Goals for Students:
    - Instead of having stretch goals for students who would be ready for them, individually assign additional requirements.
    - For these students, they should set up their projects in a way that it is already testable. Setup tests. Write TDD fashion.
    - These students should maintain their routes in an external express router module.
    - These students should utilize an external data module that creates the es client connection.
- Notes for All Students:
    - Students will learn and practice using the ElasticSearch server and node library.
    - Students do not need to get stuck with express, and router module issues.
    - Students do not need to get stuck with abstracting the data layer.
    - Students do not need to get stuck with promise issues.
    - Students are expected to understand how to write a standalone node script (for seeding the db).
    - Students are expected to already understand what code needs to be written to transform the seed data into the desired format before seeding.
    - Students should not ask how to do certain queries, they need to develop the habit of checking the docs. You should know what questions they may have where the answer could be found in the docs. ElasticSearch has great api and examples.
- Notes for Instructors:
    - It is not important for students to use _the same_ api endpoints that has been used in the example completed exercise. Students are free to design their own api endpoints in a way they can use it to display results on a browser. Students should whiteboard their api endpoints and get it approved by an instructor before implementing the api. Students shoud think critically about the capabilities and limitations of their design, will it suffice for their use case? what would a theoretical ui be capable of displaying?
    - The completed exercise should be used by instructors as a working example of es queries, _not_ of good api design. The primary limitations of the example completed exercise is that only one type of query is allowed at any one time, two types of queries cannot be created at the same time (ex: name starts with 'py' and stat hp is greater than 50). This should be the goal for beginners.
    - Students should get stuck on, and have many questions only regarding:
        - how to install and run the ElasticSearch server
        - using the `'elasticsearch'` node module
        - creating an es client connection from node to es server
        - testing/validating the client connection is made
            - use `client.ping()`
        - what should the seeded data look like
            - same as the json file, except with numbers parsed
        - how do you validate your seeded data?

            ```
            curl -XGET 'http://127.0.0.1:9200/_search?pretty=true' -d '
            {
                "query" : {
                    "matchAll" : {}
                }
            }'
            ```

# Additional Resources

#### Query DSL
- Link: [https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html)
- Notes: lucene syntax is supported in `q` queries.

#### bodybuilder
- Link: [https://github.com/danpaz/bodybuilder](https://github.com/danpaz/bodybuilder)
- Notes: Use as an exercise before DevLeague Exercise

#### ESQ (Elasticsearch Query)
- Link: [https://github.com/holidayextras/esq](https://github.com/holidayextras/esq)
- Notes: Use as an exercise before DevLeague Exercise
