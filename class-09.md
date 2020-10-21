## API Server

### Review, Research, and Discussion

**How does route prefixing work with an external routing module?**
_Route grouping is a concept to make the route function that receive same prefix of different requests. The route is being handle from route group._

**When routing, what’s the difference between app.get('/data/:id') and app.get('/data/:name')?**
_the difference is that one is dealing with id and the other is dealing with name in the request params to get data_

**Explain how Express handles routing conflicts?**
_routs will executed in order_

**What are the ways that a browser can send “data” or request variables to an HTTP server?**
_using jquery,ajax_

### Vocabulary Terms

- **Routing:** _How an application’s endpoints (URIs) respond to client requests._
- **Route Prefixing:** _Is a concept to make the route function that receive same prefix of different requests._
- **Request “Body”:** _Data sent by the client to your API._
- **Request “Query”:** _This property is an object containing a property for each query string parameter in the route._
- **Request “Params”:** _This property is an object containing properties mapped to the named route “parameters”._

### preperatiom material

### Express routing parameters

- Express lets you run middleware only when certain parameters are present and expected.

### Sub Documents Mongoose

- Mongoose is a schema driven ORM(), which fives the oppurtunity to provide structure to our Mongo documents. By default Mongo DBs are not structured and monfoose helps with that.

- Sub dosucments are great for supportive data sucha s comments on a blog post, but they're not "populated" unless you do this manually.

### joining data/documents in Mongo.

_populate is a method we can use in Mongoose to connect 2 collections._

- Methods 1: physically joining using a reference to another collection.
- Method 2: Virtual Population
  - create a virtual field in a document pointed to a field in another one.
  - In pre('find') you do a collection "on the fly" which can be more efficient than storing the relation.
- Pre and Post hooks (middleware)

  - Mongoose allows you to inject logic at various points in the lifecycle of a data record.
  - User can perform validation, normalization.

  ### Direct Population (References)

  _Create a reference column in the collection and then when you save, you need to push() into the reference field with the \_id of the referenced document. This results in quicker find() but requires a lot more management on saves, updates, deletes._

  ```
  const personSchema = Schema({
  \_id: Schema.Types.ObjectId,
  name: String,
  age: Number,
  stories: [{ type: Schema.Types.ObjectId, ref: 'Story' }]
  });
  ```

```
const storySchema = Schema({
author: { type: Schema.Types.ObjectId, ref: 'Person' },
title: String,
fans: [{ type: Schema.Types.ObjectId, ref: 'Person' }]
});

```

### Virtual Joins

_In this example, we create a virtual field in teams called players by connecting them with named fields, and then doing a populate as we find/load documents. This “join” happens in real time, as the records are being processed by Mongoose and can be quite slow, although convenient._

```
const teams = mongoose.Schema({
name: { type:String, required:true },
}, { toObject:{virtuals:true}, toJSON:{virtuals:true} });

teams.virtual('players', {
ref: 'players',
localField: 'name',
foreignField: 'team',
justOne:false,
});

teams.pre('find', function() {
this.populate('players');
});

```
