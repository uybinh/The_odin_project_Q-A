# ActiveRecord Basic

* What is an **ORM**?
ORM stands for **Oject-Relational-Mapping**
  * ORM is a technique that let you query and manipulate data in a database using an object-oriented paradigm.
  * When talking about ORM,  we usually are referring to a *library* that implements the ORM technique, hence the phrase “an ORM”.
  * ORM library is just a normal library *(written in any language of choice)* that incapsulates the code needed to manipulate the data in database.

* Why is Active Record more useful than just using SQL?

* Active Record smooths all the differences between different types of database

* When switching from one database to another, you don’t need to change any major application code, just some configuration files. 

* What are the two steps required to make a new row in your database table with ActiveRecord?
  1. Create *new* model object in memory
  2. *Save* the object into database

* What are “generators” in Rails?