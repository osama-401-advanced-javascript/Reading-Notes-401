### Review, Research, and Discussion

- Explain what a “Singleton” is (in Computer Science terms)?
  _A singleton is a class that allows only a single instance of itself to be created and gives access to that created instance. It contains static variables that can accommodate unique and private instances of itself. It is used in scenarios when a user wants to restrict instantiation of a class to only one object. This is helpful usually when a single object is required to coordinate actions across a system_

- Explain how the Singleton pattern can be used with Node modules, specifically with classes?
  _Sometimes you need to make sure that you have one and only one instance of an object. This is where the singleton pattern can be useful. A singleton represents a single instance of an object. Only one can be created, no matter how many times the object is instantiated. If there’s already an instance, the singleton will create a new one. Let’s take a look at where creating multiple instances of one object might create problems within our application._

```
class Logger {

    constructor() {
        this.logs = [];
    }

    get count() {
        return this.logs.length;
    }

    log(message) {
        const timestamp = new Date().toISOString();
        this.logs.push({ message, timestamp });
        console.log(`${timestamp} - ${message}`);
    }

}

module.exports = Logger;
```

### Vocabulary Terms

**Router Middleware :** _Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router()._

**Dynamic Module Loading :** _The dynamic module loader library allows code to retrieve Node modules from a web server, install them locally and serve them up as though they'd been manually deployed to the running server._

**Singleton Pattern :** _a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton._

**Mock Testing:** _an approach to unit testing that lets you make assertions about how the code under test is interacting with other system modules._

### Preparation Materials

### Securing Passwords

_Passwords are the first line of defense against cyber criminals. It is the most vital secret of every activity we do over the internet and also a final check to get into any of your user account, whether it is your bank account, email account, shopping cart account or any other account you have._
_We all know storing passwords in clear text in your database is ridiculous. Many desktop applications and almost every web service including, blogs, forums eventually need to store a collection of user data and the passwords, that has to be stored using a hashing algorithm._

### Basic Auth

_n the context of an HTTP transaction, basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic <credentials>, where credentials is the Base64 encoding of ID and password joined by a single colon :._

### Intro to JWT

_JSON Web Token (JWT) is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA._

### OWASP auth cheatsheet
