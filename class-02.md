## Classes, Inheritance, Functional Programming

## Sources



- Why would you want to run JavaScript code outside of a browser?
  Running JavaScript without/outside a browser means you are using node.js technology to execute your JavaScript code. This type of usage of javascript typically refers to backend programming where your javascript code will interact with your database and can be used to create RESTful APIs.

What is the difference between a module and a package?
  A package is a file or directory that is described by a package.json file.
A module is any file or directory in the node_modules directory that can be loaded by the Node.js require() function.
Note: Since modules are not required to have a package.json file, not all modules are packages. Only modules that have a package.json file are also packages.

- What does the node package manager do?
 npm, short for Node Package Manager, is two things: first and foremost, it is an online repository for the publishing of open-source Node.js projects; second, it is a command-line utility for interacting with said repository that aids in package installation, version management, and dependency management. A plethora of Node.js libraries and applications are published on npm, and many more are added every day. These applications can be searched for on http://npmjs.org/. Once you have a package you want to install, it can be installed with a single command-line command.


## Vocabulary

**ecosystem**
  - Node.js came into existence when the original developers of JavaScript extended it from something you could only run in the browser to something you could run on your machine as a standalone application..

**Node.js**
  - Node.js came into existence when the original developers of JavaScript extended it from something you could only run in the browser to something you could run on your machine as a standalone application..

**V8 Engine**
  - V8 is Google’s open source high-performance JavaScript and WebAssembly engine, written in C++. It is used in Chrome and in Node.js, among others. It implements ECMAScript and WebAssembly.

**module**
  - Module in Node. js is a simple or complex functionality organized in single or multiple JavaScript files which can be reused throughout the Node. js application. Each module in Node.

**package**
  - A package is a folder tree described by a package.json file. The package consists of the folder containing the package.json file and all subfolders until the next folder containing another package.json file, or a folder named node_modules.

**node package manager**
  - npm, short for Node Package Manager, is two things: first and foremost, it is an online repository for the publishing of open-source Node.js projects; second.

**server**
  - The HTTP module can create an HTTP server that listens to server ports and gives a response back to the client.

**environment**
  - Node. js provides a global variable process. env , an object that contains all environment variables available to the user running the application. It is expecting the hostname and the port that the app will run on to be defined by the environment.

**interpreter**
  - Interpreter coverts each high-level program statement, one by one, into the machine code, during program run. Compiled code runs faster while interpreted code runs slower.

**compiler**
  - Compiler transforms code written in a high-level programming language into the machine code, at once, before program runs

## preparation material 
## Context
*Context is related to objects. It refers to the object to which a function belongs. When you use the JavaScript “this” keyword, it refers to the object to which function belongs.*

## Classes
*Classes are a template for creating objects. They encapsulate data with code to work on that data. Classes in JS are built on prototypes but also have some syntax and semantics that are not shared with ES5 class like semantics.*

## Inheritance
*JavaScript is a bit confusing for developers experienced in class-based languages (like Java or C++), as it is dynamic and does not provide a class implementation per se (the class keyword is introduced in ES2015, but is syntactical sugar, JavaScript remains prototype-based).*

*When it comes to inheritance, JavaScript only has one construct: objects. Each object has a private property which holds a link to another object called its prototype. That prototype object has a prototype of its own, and so on until an object is reached with null as its prototype. By definition, null has no prototype, and acts as the final link in this prototype chain.*

*Nearly all objects in JavaScript are instances of Object which sits on the top of a prototype chain.*

