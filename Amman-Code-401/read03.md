# Express REST API

## Name 3 real-world use cases where you’d want to change the request with custom middleware?

1. Using `express.urlencoded` to parse the request body from forms.
2. Using authentication middlewares to show and hide specific information to the user according to its authorization access.
3. Using cookie parser to parse Cookie header and populate req.cookies with an object keyed by the cookie names.

## True or false: The route handler is middleware?

The route handler is considered the last middleware of the route method. It does not have to call the next function since it is the last one.

## In what ways can a middleware function end the process and send data to the browser?

If we called the next function with an argument or throw and error, we would end the middleware sequence.

## At what point in the request lifecycle can you “inject” middleware?

* We can inject the middleware globally using `app.use(middleware)`. Here, the middleware will be executed to perform actions on all routes and methods. It will be the first thing to run in the method handler.
* We can also inject it between the route path and the method handler inside each route we create. It will only apply to the handler that it was injected in.

## What can cause express to throw an error with “Request headers sent twice, cannot start a second response.”

If one of the middleware items writes to the response body or headers but doesn't call `response.end()` and you call `next()`, then as the core Server.prototype.handle method completes, it's going to notice that:

* no more items in the stack
* that `response.headerSent` is true

## Terms

1. Middleware: it is a script that contains some code or functions that modify the behavior of the method handler. It manipulates the request and adds some more functionality to the overall callback.
2. Request Object: It is passed to the route handler by default, and it contains different properties that determine the request behavior. It contains data like the headers, the request's path, the request's body, the URL to hit, and more.
3. Response Object: it is a default object passed to the route handler argument list. It contains the response from the server and how it should be sent to the user. It contains data like status code, response body, URL, server address, and more.
4. Application Middleware: they are middlewares that are applied to the whole application, and they will be called every time a route is hit or a request being sent.
5. Routing Middleware: they are middlewares added to a specific route or group of routes and method handlers. They only modify the routes and methods they are injected in, not all routes.
6. Test-Driven Development: it is a programming style that ensures that the application we build is working properly without problems. The results that are delivered to the clients are of high quality. It requires performing a different test to the application's functionalities called the unit tests, which means that we should test all functions and pieces of code of our application with all possible cases that the user might encounter during dealing with the application.
7. Behavioral Testing: Behavioural Testing is a testing of the external behavior of the program, also known as black-box testing. It is usually functional testing. It is a branch of Test Driven Development (TDD). BDD uses human-readable descriptions of software user requirements as the basis for software tests.

### Which three things had you heard about previously and now have better clarity on?

1. Middlewares
2. Using regex in the route path
3. Express routes chaining

### Which three things are you hoping to learn more about in the upcoming lecture/demo?

1. Testing
2. Classes
3. Node

### What are you most excited about trying to implement or see how it works?

Implementing a full functioning website with unit tests for all functionalities and seeing the 100% on the screen
