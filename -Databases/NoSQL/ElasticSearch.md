# ElasticSearch


## Terms


## DSL

https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl.html

- lucene syntax is supported in `q` queries

Introduce utilities and helper libraries, though start with raw es.

https://github.com/danpaz/bodybuilder
https://github.com/holidayextras/esq

students should practice lots of reading and navigating the well-written documentation



## Topics

- [teach] installing and turning on an elasticsearch db
- [teach] creating an elasticsearch client
- [about] streaming logs, trace vs. error
- [about] using the elasticsarch server api with curl
- [teach] using the elasticsarch node client and library api
- [teach] creating a seed script
    - use npm scripts
    - write a separate utility in a separate subdirectory
    - document how to use the utility in the readme
    - data formatting, use Numbers
- [teach] understand that in es, search size default is 10
- [teach] learning search query syntax
- [teach] get the source document from search result in js
- [grok] documents https://www.elastic.co/guide/en/elasticsearch/guide/current/document.html

## Exercise

Completed Exercise: https://github.com/theRemix/Springy-Findeon

Instead of having stretch goals for students who would be ready for them, individually assign additional requirements.

For these students, they should set up their projects in a way that it is already testable. Setup tests. Write TDD fashion.

These students should maintain their routes in an external express router module.

These students should utilize an external data module that creates the es client connection.

For all students:

Students will learn and practice using the ElasticSearch server and node library.

Students do not need to get stuck with express, and router module issues.

Students do not need to get stuck with abstracting the data layer.

Students do not need to get stuck with promise issues.

Students are expected to understand how to write a standalone node script (for seeding the db).

Students are expected to already understand what code needs to be written to transform the seed data into the desired format before seeding.

Students should not ask how to do certain queries, they need to develop the habit of checking the docs. You should know what questions they may have where the answer could be found in the docs. ElasticSearch has great api and examples.

It is not important for students to use _the same_ api endpoints that has been used in the example completed exercise. Students are free to design their own api endpoints in a way they can use it to display results on a browser. Students should whiteboard their api endpoints and get it approved by an instructor before implementing the api. Students shoud think critically about the capabilities and limitations of their design, will it suffice for their use case? what would a theoretical ui be capable of displaying?

The completed exercise should be used by instructors as a working example of es queries, _not_ of good api design. The primary limitations of the example completed exercise is that only one type of query is allowed at any one time, two types of queries cannot be created at the same time (ex: name starts with 'py' and stat hp is greater than 50). This should be the goal for beginners.

Students should get stuck on, and have many questions only regarding:

- how to install and run the ElasticSearch server
- using the `'elasticsearch'` node module
- creating an es client connection from node to es server
- testing/validating the client connection is made
    - use `client.ping()`
- what should the seeded data look like
    - same as the json file, except with numbers parsed
- how do you validate your seeded data
    - curl
        ```
        curl -XGET 'http://127.0.0.1:9200/_search?pretty=true' -d '
        {
            "query" : {
                "matchAll" : {}
            }
        }'
        ```

