## TCP Servers

### Review, Research, and Discussion

- **what are some examples of back-end events?**
  _Backend events are Freshdesk product events such as ticket create, ticket update, and note create that trigger backend app._

* **Why are events sometimes better than asynchronous actions with callbacks?**
  _An event handler is a type of callback. It's called whenever an event occurs. The term is usually used in terms of user interfaces where events are things like moving the mouse, clicking something and so on._

* **What does an EventEmitter instance do?**
  _All objects that emit events are instances of the EventEmitter class. These objects expose an eventEmitter.on() function that allows one or more functions to be attached to named events emitted by the object. Typically, event names are camel-cased strings but any valid JavaScript property key can be used._

* **When is a program’s call stack, event queue, and event loop active?**
  _The main event loop is the one that is running on the main thread, it is the only active event loop when the application starts, and it remains active until the application ends._

_having one is to keep track of the point to which each active subroutine should return control when it finishes executing._

### Vocabulary Terms

- **Observer Pattern:** _software design pattern in which an object, called the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods._

- **Listener:** _must implement the interface for the event it wants to listen to._

- **Event Handler:** _software routine that processes actions such as keystrokes and mouse movements._

- **Event Driven Programming:** _programming paradigm in which the flow of the program is determined by events such as user actions, sensor outputs, or messages from other programs or threads._

- **Event Loop:** _programming construct or design pattern that waits for and dispatches events or messages in a program._

- **Event Queue:** _repository where events from an application are held prior to being processed by a receiving program or system._

- **Call Stack:** _stack data structure that stores information about the active subroutines of a computer program._

- **Emit/Raise/Trigger:** _function raises the specified event._

- **Subscribe:** _one where providers that supply not only network access and a foundation suite of applications, but also the complete user environment—including all customer premises equipment—as a package for a monthly subscription._

- **database:** _data structure that stores organized information._

### Preparation Materials

### Event Queues

- Much of the NodeJS architecture is built around the use of events. All objects that emit events in NodeJS are instances of the EventEmitter constructor. EventEmitters are a great way to handle controlling asynchronous events. Functions can be registered as listeners for an event on instances of the EventEmitter class. These instances can emit events and pass the listener's data.

* In practical applications, multiple "disconnected" services can communicate with one another using various protocols using proprietary APIs. Generally, this is done through a central "Hub" server (or Queue) which receives all inbound messages, scrubs the content, and then broadcasts those messages to connected subscribers.

**OSI Model**

- Programmers and engineers have been able to network computers since the early 1970s. As the needs of networked computers evolved, there were many solutions developed to connect two or more computers together and share information between them. Over time, several different conceptual models have also been developed to help describe the different networking solutions. In the mid 1980s the "Open Systems Interconnection Reference Model" (OSI Model) was developed as a seven layer model. This seven layer OSI model has continued to accurately describe the different processes in computer networking, and is still widely used as a point of reference while working in networked systems today. A developer or engineer is usually responsible for the goals of a specific layer and communication with the layer above and below. Not every computer network solution uses all seven layers, for example HTTP skips the presentation and session layers and lives directly on top of the transport layer.

**Internet Protocol Suite**

- The internet Protocol Suite is the conceptual model for the protocols used by the internet. It is often referred to as TCP/IP because the IP and the TCP were the original protocols in the suite. The Internet Protocol Suite is described using four layers - Link, Internet, Transport, and Application. Web developers often reference the Internet Protocol Suite model when discussing network communication and data exchange.

**TCP**

- The Transmission Control Protocol is widely used by applacation layer protocols in the Internet Protocol Suite. TCP creates a two way communication between two hosts and provides reliable, ordered, and error checked byte streams between the applications. TCP data transfers manage network congestion and use flow control to limit the rate a sender transfers data to guarantee reliable delivery. Each IP packet between the hosts carries a single TCP Segment. A TCP segment is made up of header and data sections.

**TCP Header**

- The TCP Header is used at each end to control the type of interaction being sent. It contains the following information:

  - a 16 bit source port

  - a 16 bit destination port

  - a 32 bit sequence number that sets the initial sequence number and manages the accumulated sequence number

  - if ACK is set, it contains a 32 bit acknowledgement number that is the next sequence number that the sender is expecting. It is used for acknowledging the bytes it has so far received

  - a 4 bit data offset specifies the size of the tcp header in 32 bit words

  - 9 flag bits

    - NS - an experimantal feature for a nonce sum - a nonce is a random cryptographic number used to prevent people from lying about who they are (authentication)

    - CWR - used to acknowledge that a TCP segment with the ECE flag has been received, and the Window has been reduced to alleviate congestion

    - ECE - if SYN is 1 it indicates that the peer is ECN capable, otherwise it is sued to indicate that there is network congestion

    - URG - indicates that the Urgent pointer filed is significant

    - ACK - indicates that the ACK fiel is significant - all packets after the initial SYN should have this flag set

    - PSH - used to ask to push the buffered data to the receiving application

    - RST - used to reset the connection

    - SYN sent only on the first packet sent from each end to synchronize the sequence numbers

    - FIN - indicates the last package from a sender, and is used in closing a connection

  - a 16 bit window size

  - a 16 bit checksum used for error checking the header

  - if URG is set it contains a 16 bit urgent Pointer

  - a variable 0 to 320 bit (divisible by 32) options section

**Connection Establishment**

- The client sends a SYN packet with a random sequence number. The server sends a SYN-ACK packet with the acknowledgement number set to one more than the initial sequence number. The client responds with and ACK and an acknowledgement number incremented by one.

**Connection Termination**

- One end sends a FIN segment and the other sends and ACK segment followed by a FIN segment. The termination initiation will then respond with an ACK segment.
