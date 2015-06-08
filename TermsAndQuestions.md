##Terms
1. Database - a place to store data

2. Collection - located within a database and contain documents. 

3. Document - contain fields and values. are located within a collection. 

4. Cursor - the address of an object in Mongo

5. Field - similar to the "property" within an object. 

6. CRUD - the idea of create, read, update and delete on a specific set of date. 

7. Relational Database - there are relationships between the sets of data. ex: author: books. 

8. Non-Relational Database - there are no relationships between the pieces of data. data is stored without order.

9. CAP Theorem -  states that it is impossible for a distributed computer system to simultaneously provide all three of the following guarantees:
    - Consistency (all nodes see the same data at the same time) 
    - Availability (a guarantee that every request receives a response about whether it succeeded or failed)
    - Partition tolerance (the system continues to operate despite arbitrary partitioning due to network failures). source: http://en.wikipedia.org/wiki/CAP_theorem

10. Schema - adds a layer of organization to your database.

##Questions

1. Do MongoDB databases have schemas?  
    - No 
2. What are typical uses for MongoDB?
    - You should not use MongoDB. 
3. What is Mongoose?
    - It is MongoDB with a schema.  
4. What is a Mongoose Model? 
    - Models are fancy constructors compiled from the Schema definitions. Instances of these models represent documents which can be saved and retreived from the database. All document creation and retreival from the database is handled by these models.