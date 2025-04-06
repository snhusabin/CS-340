
About the project


This Python-based module provides full CRUD (Create, Read, Update, Delete) functionality to manage animal records in a MongoDB database. Designed specifically for Grazioso Salvare, an animal rescue organization, this module allows both developers and staff to interact with shelter data through secure and reusable code. It enables the addition, retrieval, editing, and removal of animal records in a centralized system, laying the foundation for future integration with dashboards or analytical tools.

Motivation
The system needed by Grazioso Salvare would not only be user-friendly but efficient in terms of keeping up with its growing list of saved animals. Rather than enter data manually or traditionally, this project was structured in a way to facilitate real-time database use through modern tools like Python and MongoDB. The idea was to simplify task management for employees, eliminate errors, and be able to visualize through a web interface or dashboard in the future.

Getting  Started
Before this module can be used in your local environment, first, Python, along with Mongo, Python's official MongoDB driver, is required. You also require your access credentials for the AAC MongoDB instance. With these in hand, you can download or clone this repository and get started with this module by importing and initializing the class AnimalShelter in your Python project.

Installation
This project's foundation is the use of the Mongo library in interacting with MongoDB. The use of this library was due to its trustworthiness, immense community support, and native Python code compatibility. It also supports front-end tools, such as Dash, so it's a potential candidate for use within dashboards.

Usage


Once instantiated, the class has total control of the animal records in MongoDB. All operations are equivalent to a raw database operation.

To add a new animal record, use the create() method and pass in a dictionary containing fields such as name, animal type, breed, and age. If the insertion is successful, the method confirms it by returning True.
 

To retrieve records, the read() method can be called with or without a query. Without arguments, it returns all records. When provided with a query, it returns a filtered list of matching documents based on the specified fields.


 

If you need to update existing records, use the update() method. It requires a query to locate the correct document(s) and a dictionary of fields to update. You can also specify whether you want to update a single record or multiple records by setting the multiple flags to True.

 

To remove records from the database, the delete() method is used. This method accepts a query to match the document(s) you want to remove. Just like with updates, you can control whether the operation deletes a single document or multiple matching ones by setting the multiple parameter to True.
 

1.Upload the Austin Animal Center Outcomes data set into MongoDB by inserting a CSV file using the appropriate MongoDB import tool.
 
 
 
2. Create a user account in the mongo shell to ensure user authentication to the database and collection you created.
 
 
 
3.
 
 


 

3. a
•	A Create method that inserts a document into a specified MongoDB database and collection
o	Input -> argument to function should be the key/value lookup pair to use with the MongoDB driver find API call.
o	Return -> “True” if successful insert, else “False”.

 
•	A Read method that queries for document(s) from a specified MongoDB database and specified collection
o	Input -> arguments to function should be the key/value lookup pair to use with the MongoDB driver find API call.
o	Return -> result in a list if the command is successful, else an empty list.
Important: Be sure to use find() instead of find_one() when developing your method. Hint: You will have to work with the MongoDB cursor returned by the find() method.

•	An Update method that queries for and changes document(s) from a specified MongoDB database and specified collection
o	Input -> arguments to function should be the key/value lookup pair to use with the MongoDB driver Find API call. The last argument to function will be a set of key/value pairs in the data type acceptable to the MongoDB driver update_one() or update_many() API call.
o	Return -> The number of objects modified in the collection.
•	A Delete method that queries for and removes document(s) from a specified MongoDB database and specified collection
o	Input -> arguments to function should be the key/value lookup pair to use with the MongoDB driver find API call.
o	Return -> The number of objects removed from the collection.
 
 
 

Contact
Author: Sabin Neupane

![image](https://github.com/user-attachments/assets/54c3e4f6-fea8-493d-b717-4feb76bcadde)
