## HTTP and REST

- What is the advantage of an ORM, like Mongoose?
  **The three main advantages of using Mongoose versus native MongoDB are:**
  1- MongooseJS provides an abstraction layer on top of MongoDB that eliminates the need to use named collections.
  2-Models in Mongoose perform the bulk of the work of establishing up default values for document properties and validating data.
  3-Functions may be attached to Models in MongooseJS. This allows for seamless incorporation of new functionality.
  4-Queries use function chaining rather than embedded mnemonics which result in code that is more flexible and readable, therefore more maintainable as well.

  - How does the repository pattern compare with an ORM?
    _An ORM is the acronym for Object-Relational Mapper and this term is a giveaway. It says clearly that it's purpose is to provide a bridge between the object oriented way(your application) and the relational way (the relational database). Pretty much any ORM will provide the application with a virtual oop representation of the database and will make it easy to CRUD without involving SQL that every developer loves. It also provides an abstraction over a specific rdbms, so it's easy to change let's say from MySQl to SqlServer with a simple config setting. However, if you want to use a NoSql db like MongoDb or RavenDb, you're out of luck. These are document databases not relational ones. An ORM is completely useless here._

_But with a RDBMS, it's very useful and it can simplify your work as a developer, especially if you don't like dealing with sql and specific db quirks. However it does come with a price: steep learning curve (it's not that easy to understand how to fully use NhIbernate or EF for example) and some performance penalties. It's also way to easy to intermingle it everywhere, forgetting that is in fact an implementation detail of how the app is persisting things(the fallacy of using the ORM model as the domain model)._

- When making a repository/facade, what flexibility do you gain?

_Over the previous chapters, you have seen a variety of persistence mechanisms. As time went on, you repeated similar code functions: initializing, creating, reading, updating, and deleting. You sometimes wrote a similar boilerplate code where the same sequence of actions was coded for different object types._

_When you carry out similar tasks not easily factored into an object, you should look to see what patterns from which you can borrow. Patterns are descriptions of common relationships and interactions between system components._

- Name 3 cloud based NoSQL Databases
  **CouchDB**
  **Redis**
  **MondoDB**

## Vocabulary Terms

**lifecycle:** is a process used by the software industry to design, develop and test high quality softwares.
**collections:** MongoDB stores documents in collections. Collections are analogous to tables in relational databases.

**the “Repository” design pattern:** The repository pattern is one of the more popular patterns at the moment. I for one like it, it follows the solid principles and done right it is clean and easy to use.

**Object Relation Mapping (ORM):** Object-relational-mapping is the idea of being able to write queries like the one above, as well as much more complicated ones, using the object-oriented paradigm of your preferred programming language.

## preparation material

**HTTP definition:**

_The Hypertext Transfer Protocol (HTTP) is a stateless application-lever protocol for distributed, collaborative, hypertext information systems. HTTP is the foundation for the world wide web._

**HTTP Requests:**

_A HTTP/1.1 request is formatted in text ant transferred using TCP (Transmission Control Protocol). The first line of the request contains the METHOD, URL, and HTTP VERSION. The following lines ar the request HEADERS. Each header is separated by a newline character. A header is a key value pair separated using a colon. headers containing more than one value separate each value using a semicolon. The header section of the request is terminated with an empty line. An optional body follows the header section._

**HTTP Response:**

_A HTTP/1.1 response is also formatted in text and transferred using TCP. The first line of the response contains the HTTP VERSION, STATUS CODE, and STATUS MESSAGE. The following lines are the request headers and are formatted exactly the same way as the request headers. The header section fo the response is terminated with an empty line. An optional body follows the header section._

**REST definition:**

_REST is an acronym for REpresentational State Transfet._ _It is a means tby which we can reference, manipulate, and transfer state._ _REST uses a common set of methods (called 'verbs") to operate on the state of a resource ("noun"), generally using HTTP as the transfer protocol._
_A "RESTful Endpoint" is a URI (Uniform Resource Identifier) that identifies the resource. When addressed with a proper method, you are able to effect state._ _In normal terms, this means "Performing CRUD operations over HTTP"._

_Generally speaking, RESTful endpoints deliver data in JSON format. The best practice is to supply a header with metadata and a collection of results._

**REST Documentation (Swagger)**

_The standard for documenting REST APIs is with a "live" documentation system: Open API (formerly "Swagger")._

_Once generated, Swagger Docs present developers a way not only to see how to use an API, but to actually use it. This documentation actually allows for live requests from within it._
