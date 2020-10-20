### Express Routing & Connected API

### Document the following Vocabulary Terms

**Middleware:** _functions are functions that have access to the request object (req), the response object (res), and the next function in the application’s request-response cycle._
**Request Object:** _The req object represents the HTTP request and has properties for the request query string, parameters, body, HTTP headers, and so on._
**Response Object:** _The res object represents the HTTP response that an Express app sends when it gets an HTTP request._

**Application Middleware:** _Bind application-level middleware to an instance of the app object_

**Routing Middleware:** _Router-level middleware works in the same way as application-level middleware, except it is bound to an instance of express.Router()._.

### Preparation Materials

### Routing

_Routing refers to how an application’s endpoints (URIs) respond to client requests_

_You define routing using methods of the Express app object that correspond to HTTP methods; for example, app.get() to handle GET requests and app.post to handle POST requests. For a full list, see app.METHOD. You can also use app.all() to handle all HTTP methods and app.use() to specify middleware as the callback function (See Using middleware for details)._

### Route handlers

_You can provide multiple callback functions that behave like middleware to handle a request. The only exception is that these callbacks might invoke next(‘route’) to bypass the remaining route callbacks. You can use this mechanism to impose pre-conditions on a route, then pass control to subsequent routes if there’s no reason to proceed with the current route._
