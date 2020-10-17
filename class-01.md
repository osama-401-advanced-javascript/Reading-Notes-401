## Node Ecosystem, TDD, CI/CD

## Array.map()
*The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.*

## Array.reduce()
The reduce() method executes a reducer function (that you provide) on each element of the array, resulting in single output value.

## superagent 
It is a client-side HTTP library for Node.js

* using .then()
```
// url is the url of the API, or a folder
// data is the results from the calling
superagent.get(url).then((data) => {
  console.log(data);
});
```
* using async/await
```
async function calling() {
  const res = await superagent.get(url);
  console.log(res);
}
```
## Promise
*A Promise is a proxy for a value not necessarily known when the promise is created. It allows you to associate handlers with an asynchronous action's eventual success value or failure reason. This lets asynchronous methods return values like synchronous methods: instead of immediately returning the final value, the asynchronous method returns a promise to supply the value at some point in the future.*

## callbacks
*A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.*

* Here is a quick example:
```
function greeting(name) {
  alert('Hello ' + name);
}

function processUserInput(callback) {
  var name = prompt('Please enter your name.');
  callback(name);
}

processUserInput(greeting);
```
*The above example is a synchronous callback, as it is executed immediately.*

*Note, however, that callbacks are often used to continue code execution after an asynchronous operation has completed — these are called asynchronous callbacks. A good example is the callback functions executed inside a .then() block chained onto the end of a promise after that promise fulfills or rejects. This structure is used in many modern web APIs, such as fetch().*

## Preparation Materials
### What is Node.js?
- Node.js is an open source server environment
- Node.js is free
- Node.js runs on various platforms (Windows,      Linux, Unix, Mac OS X, etc.)
- Node.js uses JavaScript on the server

## Why Node.js?
*A common task for a web server can be to open a file on the server and return the content to the client.*

*Here is how PHP or ASP handles a file request:*

1- Sends the task to the computer's file system.
2-Waits while the file system opens and reads the file.
3- Returns the content to the client.
4- Ready to handle the next request.

*Here is how Node.js handles a file request:*

1- Sends the task to the computer's file system.
2- Ready to handle the next request.
3-When the file system has opened and read the file, the server returns the content to the client.

*Node.js eliminates the waiting, and simply continues with the next request.*

*Node.js runs single-threaded, non-blocking, asynchronously programming, which is very memory efficient.*

