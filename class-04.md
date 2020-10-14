## Advanced Mongo/Mongoose



- Why would a developer choose to make data models?

  - A data model ensures that when you create the db you don't forget any data that needs to be included.

- What purpose do CRUD operations serve?

  - CRUD operations sum up the functions that users need in order to create and manage data.

- What kind of database is Postgres? What kind of database is MongoDB?

  - Postgres is a SQL database.

  - MongoDB is a NoSQL database.

- What is Mongoose and why do we need it?

  - An Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation and is used to translate between objects in code and the representation of those objeces in MongoDB.

- Define three related pieces of data in a possible application. An example for a store application might be Product, Category and Department. Describe the constraints and rules on each piece of data and how you would relate these pieces to each other. For example, each Product has a Category and belongs in a Department.

- In a car application, we might need to know the Make, Model, and Engine Size, of each car. We know that every car has an engine, as well as a Make, and a Model. I'm not sure what you mean by constraints and rules on each piece of data. 

## Vocabulary

**database**

  - An electronic system that allows data to be easily accessed, manipulated, and updated.

**data model**
  
  - A data model documents and organizes data, how it is stored and accessed, and the relationships among different types of data. 

**CRUD**

  - CRUD stands for create, read, update, and delete. These are the four basic functions of persistent storage.

**schema**

  - A schema is an outline, diagram, or model. Schemas are often used to describe the structure of different types of data.

**sanitize**

  - To deliberately, permanently and irreversibly remove or destroy the data stored on a memory device to make it unrecoverable.

**Structured Query Language (SQL)**

  - A domain-specific language used in programming and designed for managing data held in a relational database.

**Non SQL (NoSQL)**

  - An alternative to traditional relational databases. NoSQL databases are expecially useful for working with large sets of distributed data.

**MongoDB**

- MongoDB is an open source database management system (DBMS) that uses a document-oriented database model which supports various forms of data.

**Mongoose**

- An Object Data Modeling (ODM) library for MongoDB and Node.js. It manages relationships between data, provides schema validation and is used to translate between objects in code and the representation of those objeces in MongoDB.

**record**

  - A record is composed of fields and contains al the data about one particular person, company, or item in a database.

**document**

  - A modern way to store data in JSON format rather than rows and columns.

**Object Relation Mapping (ORM)**

  - A mechanism that makes it possible to address, access, and manipulate objects without having to consider how those objects relate to their data sources.

## Preparation Materials (Links to an external site.)
## Repository Design Pattern
*Repository pattern separates the data access logic and maps it to the business entities in the business logic. (business logic accesses the data object without having knowledge of underlying data access architecture).*

*Using repositories as an interface will not limit you to connect to one ORM or database. it gives flexibility to your applicatio*


## In Memory Database Testing (Links to an external site.)
 *in memory database turned out to be perfect to test applications where the logic is mainly handled through database operations and where the memory and execution time are not an issue.*