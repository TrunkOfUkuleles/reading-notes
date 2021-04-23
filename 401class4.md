

### QUESTIONS

1. Name 3 advantages to Test Driven Development
    Start at a functional level - can be a good roadmap
    see breaks more quickly
    allows for more agile development

2. In what case would you need to use beforeEach() or afterEach() in a test suite?
    When working in a read DB environment, you need to be able to add things to the DB to test functionality. The before and after adds whatever is needed, and cleans them up fron the db after. 

3. What is one downside of Test Driven Development
    conceptually more complicated

4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
    The ES6 class was designed to add more usability for other programmers of other languages. Where the constructor adds a lot more code, the class structure gives you more ways to modularize down.
5. Why REST?
    RESTful is the practive of having a standardized set of action can be reliably called upon on the web. 


### Vocabulary

Functional programming: Bind to mathmatical style of functions. What to solve, not how.

object-oriented programming (OOP): STructure where you build objects to build other objects.

class: an inheritor type added to ES6

super: denotes the props being passed down through constructor

this: relative reference to the current environment

Test Driven Development (TDD): Lead with tests to pass, and build functionality accordingly.

Jest: testing platform 

Continuous Integration (CI): Process by which you can integrate updates to the system after going up.

REST: Represntational State Transfer using HTTP for CRUD

Data Model: Abstract model that organizines and standardizes data and their relationships

## Preview
- Which 3 things had you heard about previously and now have better clarity on? 
    SQL and what it looks like. I have used it before, but I didn't go too deep into relational systems

- Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    if i like one more than the other, msql vs postgreSql, how to start confidently

- What are you most excited about trying to implement or see how it works?
    how weird NoSQL can get


### SQL Vs. NoSQL

SQL is the classic Relational Database - Structured Query Language. Data kept in databases with columns of data matching a schema. You need to have the same structure across the different entries to the db. It gets powerful where you track multiple dbs, and relationships to each other - many to many, one to one, one to many (like user housing multiple data_id references), many to many.

MongoDB has DBs, but then house collections with different schemas - not keeping the same values. More complicated as things grow, but is way more flexible. There are no reltions build into this system. have alkl the info into one place. way more duplication. 

## Horizontal vs Vertical
Horizontal scaling - SQL does not support because adding harware would mean handling splitting data up. 
Vertical - making the server/hardware stronger. this is where SQL takes an edge. As things grow SQL becomes more useful. 

