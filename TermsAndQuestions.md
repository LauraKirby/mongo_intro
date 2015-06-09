##Terms
1. Database - a place to store data

2. Collection - located within a non-relational database and in MongoDB they contain a document(s). 

3. Document - contain fields and values.It is an object that sits inside a collection.

4. Cursor - the address of an object in Mongo. It is a pointer to a document object. This gives Mongo it's speed.
    - You can obtain the object by using findOne or using toArray (see example below)
    - Ex: db.people.find().toArray()[0].name
    - Cursors are useful for just reading and seeing. Do not use when you need to modify the object. 
    

5. Field - similar to the "property" within an object. 

6. CRUD - the idea of create, read, update and delete on a specific set of date.  

7. Relational Database - there are relationships between the sets of data/tables. tabke for authros and table for books and they are related. 
    - Normilization - separating your data into tables. Isolation peices of information into to subset of information 
    - Schema - pieces of data in a table that you can work with.

8. Non-Relational Database - there are no relationships between the pieces of data. data is stored without order.
    - a faster look-up  
    - easier to work with when you have larger data sets or **use when are unsure of your the data that you will be working with**

9. CAP Theorem -  states that it is impossible for a distributed computer system to simultaneously provide all three of the following guarantees:
    - Consistency (all nodes see the same data at the same time) 
    - Availability (a guarantee that every request receives a response about whether it succeeded or failed)
    - Partition tolerance (the system continues to operate despite arbitrary partitioning due to network failures). source: http://en.wikipedia.org/wiki/CAP_theorem
    - Review: http://robertgreiner.com/2014/08/cap-theorem-revisited/
    - No database is great at all three. 

10. Schema - adds a layer of organization to your database.
	- a way that your data is organized. the way to think about your data, how i structure my data

##Questions

1. Do MongoDB databases have schemas?  
    - Yes, but it is a flexible schema, which really means you can organize the data in anyway you want. 
2. What are typical uses for MongoDB?
    - Somethings. Ex: games - when you have larger sets of data that you are unsure of the data you will receive. When you have many logs to a database.  
3. What is Mongoose?
    - It is MongoDB with a schema. It is object modeling for node.js
4. What is a Mongoose Model? 
    - Models are fancy constructors compiled from the Schema definitions. Instances of these models represent documents which can be saved and retreived from thegit  database. All document creation and retreival from the database is handled by these models. Source: http://mongoosejs.com/docs/models.html
    - the model is the class. if you have a model, then you make a schema out of that. You are going to create instances of that schema through that 
    models put a name to the schema