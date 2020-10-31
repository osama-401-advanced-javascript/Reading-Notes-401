## Event Driven Applications

### Review, Research, and Discussion

- **Why is access control important?**
  _it helps in avoiding conflicts with the users also its make the website more organize_

- **Describe an application that would need access control.?**
  _UBER application the coustmer need an access different than that the driver use_

- **What is a role used for.?**
  _to determine the level of authority for each user_

### Vocabulary Terms

- **Authorization :** _Authorization is the next step in the login process, which determines what a user is able to do and see on your website. Once a user’s identity has been verified through the authentication process, authorization determines what permissions they have._

* **Role Based Access Control :** _Role-based access control (RBAC) is a method of restricting network access based on the roles of individual users within an enterprise. RBAC lets employees have access rights only to the information they need to do their jobs and prevents them from accessing information that doesn't pertain to them._

* **Capabilities :** _is a communicable, unforgeable token of authority. It refers to a value that references an object along with an associated set of access rights. A user program on a capability-based operating system must use a capability to access an object._

### Preparation Materials

### Event Driven Programming

- Nearly everything in the world is "Event Driven".

- Humans respond to events billions of times every day. Your eyes react to light. You hit the brakes when the car in front of you slows down. Your skin forms a blister when burned, etc.

* Machines can be event driven as well. Self driving cars can stay in their lane by "reading" the road lines in real time. Thermostats constantly turn the heat/air on or off in response to the temperature.

* How can we leverage this in a software application?

  - Everything in JS is an object

  - Most actions in JS are event driven

    - UI Events

    - Express Routes

    - (soon) Model Lifecycle Hooks

    - (later) React...everything.

  * Now, we harness that power

**Emitting Events**

- Node.js natively provides us with a useful module called EventEmitter that allows us to get started incorporating Event-Driven Porgramming in our project right away. Of course, creating our own version of EventEmitter wouldn't be much of a chalenge, and in fact there are several modules published on npm such as EventEmitter2 and EventEmitter3 which promise a faster performance than the native EventEmitter.

* We access the EventEmitter class through the events module. Once imported, we'll need to create a new object from the class to start using it.

```
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```

- Now we can get started with Event-Driven Programming in Node.

* Next, we'll need to create an event listener for whatever event we're expecting, then we can use EventEmitter's on methot to set the listener.

* EventEmitter has an emit methot that we use to trigger the event.

**Removing Listeners**

- There will likely come a time when you want to remove an event listener from an event. This could be for performance reasons (the event is no longer needed) or to avoid memory leaks (if an event listener references an obhject that is no longer needed, it won't be able to be "garbage-collected". This could lead to a build up of unnecessary objects).

* To remove event listeners in EventEmitter, we can use the removeListener or removeAllListeners methods. It's important to note that in the EventEmitter that comes built-in with Node, you must pass a reference to the exact function you wish to remove, when using the removeListener method. This means that wherever you wish to remove the event, you'll need to make sure the function is able to be referenced from that place in your code. For this reason, it is often best to name your event handling functions and declaring them before you register the event listener, as opposed to leaving them anonymous.

**OOP + Event-Driven Programming**

- Combining OOP and Event-driven programming paradigms make for a very valuable combination in a wide variety of situations.

- The Object Oriented approach promotes the idea that all behavior of an individual unit (or object) be handled from the code within that unit. Using this approach, applications are built with many different units that all speak to and interact with eachother.

- By registering event listeners, we can actually reverse the flow of communication between our objects. Rather than an object needing to "reach inside" another object to trigger a function, our objects can just emit events and whichever objects are listening to those events will process them in the way they have been told to. The source of an object's behavior is now entirely contained within itself, rather than needing to be accessed by external objects.
