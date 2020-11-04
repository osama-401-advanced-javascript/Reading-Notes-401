## Message Queues

### Review, Research, and Discussion

- **What does it mean that web sockets are bidirectional? Why is this useful?**
  _Whereas HTTP relies on a client request to receive a response from the server for every exchange,WebSockets allow for full-duplex bidirectional communication. This enables the server to send real-time updates asynchronously, without requiring the client to submit a request each time. In the context of networked AV and control systems_

* **Does socket.io use HTTP? Why?**
  _The client will try to establish a WebSocket connection if possible, and will fall back on HTTP long polling if not._

* **Can a socket server application have multiple socket connections?**
  _Can share the same server-side IP/Port pair as long as they are associated with different client-side IP/Port pairs_

* **What happens when a client emits an event**
  _it will trigger for a listener for this event_

### Document the following Vocabulary Terms

- **Web Socket :** _The communication protocol that allows a client and a server to connect over a TCP protocol. The Web Socket remains open to allow real time data transfer._
- **Socket.io :** _Socket.io broadcasts mulitple sockets at a time, and it works on all platforms._
- **Client :** _The client is the one asking for information or data, and the server is providing it._
- **Server :** _A server provides functionality, data, and information to clients. A single server can serve mulitple clients._

### Preparation Materials

**Socket.IO is composed of two parts:**

- A server that integrates with (or mounts on) the Node.JS HTTP Server socket.io
- A client library that loads on the browser side socket.io-client

  **During development, socket.io serves the client automatically for us, as we’ll see, so for now we only have to install one module:**

`npm install socket.io`

### Emitting events

_The main idea behind Socket.IO is that you can send and receive any events you want, with any data you want. Any objects that can be encoded as JSON will do, and binary data is supported too._

_Let’s make it so that when the user types in a message, the server gets it as a chat message event. The script section in_
`index.html `should now look as follows:

```
<script src="/socket.io/socket.io.js"></script>
<script src="https://code.jquery.com/jquery-3.4.1.min.js"></script>
<script>
 $(function () {
   var socket = io();
   $('form').submit(function(e) {
     e.preventDefault(); // prevents page reloading
     socket.emit('chat message', $('#m').val());
     $('#m').val('');
     return false;
   });
 });
</script>
```
