### SQL

Structured Query Language. SELECT id,name,price FROM products basic commands. Get, Put etc

 good for tables. Product tables, etc. Very strict requirements and how they are entered

 ## Schima
 fields(columns)
 records(rows)

 all entries share the same schema - even if they are empty. Use multiople relational tables that are all doing information processing to get info from many different APIs. YOU can have tables setting relations between other tables to give complexity to a rigid data struicture. 

 ## Many-to-many one-to-one
 Types of relations. Where a record has a single master id to track across the system (121). for a system where products are assignmed cretor ids we have a tracking system where one user has a single id, but can be a parent of multiple products (12many). multiple roles and ids need a user role s master table to track the matches - many to many is complicated.   


### NoSQL - MongoDB

less relational data, more attaching the information needed in each collection so they have to merge way less often. Means it gets bigger and is more clumsy to update. No SChima means less angry errors, but you can't be sure the shape of data you are getting at any one time. Good for projects with a lof of read actions, but not many writes.

### Horizontal / Vertical Scaling

SQL doesn't like horizontal. Spliting the database across servers no go. Vertical gives a larger and more powreful server to run off us, but those expenses are more immediate. 

Also Redis is good