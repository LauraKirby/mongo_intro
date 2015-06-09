Write the queries necessary to perform the following tasks

1. Write the terminal command to start the mongo server: mongo 

2. Write the terminal command to enter a mongo shell: use

3. Show all databases: show dbs

4. Use the library database: use library

5. Show all the collections inside the library database: show collections 

6. Using the insert method Add an author with the name of "John", age of 37: **db.authors.insert({name:"John", age:37})**

7. Using the insert method Add another author with the name of "Jane", age of 42 and give her a property of books which is an empty array. **db.authors.insert({name:"Jane", age:33, books: []})**

8. Using the .save() method, find an author with an age greater than or equal to 42 and then change the age to 33. Finally, save that author. Notes: User a filter, which begins with $, to find if greater than. **db.authors.findOne({age:{$gt: 33}})**


9. Find all of the authors: **db.authors.find()**

10. Find an author with the name of John: **db.authors.find({name:"John"})**
11. Find all of the authors but limit the search to one: **db.authors.findOne()**
12. Find an author whose name is not equal to "John" using the $ne operator: **db.authors.findOne({name:{$ne: "John"}})**
13. Update an author who has a name of "John" and change his name to "James" (without using the set method: **db.authors.update({name:"John"},{name:"James"})**
14. Update an author named "James" and using the set operator, set his name back to John and age to 37: **db.authors.update({name:"bob"},{$set:{name:"John", age:37}})**
15. Delete an author whose name is "John": **db.authors.remove({name: "John"})**
16. Delete all of the authors: **db.authors.remove({})**
17. Create an author whose name is "John" and has an empty array of books **db.authors.insert({name:"John", books: []})**
18. Update John and Using the $push operator add the string "Of Mice and Men" into the books array. **db.authors.update({name:"John"},{$push:{books: "Of Mice and Men"}})**
19. Update John and using the $push and $each operators add the strings "Grapes of Wrath", "The Pearl", "East of Eden", "50 Shades of Gray" into the books array. **db.authors.update({name:"John"},{$push:{books:{$each:["Grapes of Wrath", "The Pearl", "East of Eden", "50 Shades of Gray"]}}})**
20. Sorry - John Steinbeck didn't write 50 Shades of Gray, using the $pull operator, remove that book from the array. **b.authors.update({name:"John"},{$pull:{books:"50 Shades of Gray"}})**  
21. Finally, using the $in operator, update an author who has a book "Of Mice and Men" and "The Pearl" in the books array and change their name to "John Steinbeck"