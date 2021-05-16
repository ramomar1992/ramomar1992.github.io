# Authentication

## Explain what a “Singleton” is

A singleton is a software engineering design pattern that uses the single instance of a class to control the instantiation of objects from the class.
We can't create more than one instance of the class, and all programming operations done by the class are managed through this single instance.
The singleton design pattern solves problems like:

* How can it be ensured that a class has only one instance?
* How can the sole instance of a class be accessed easily?
* How can a class control its instantiation?
* How can the number of instances of a class be restricted?
* How can a global variable be accessed?

The singleton design pattern describes how to solve such problems:

* Hide the constructor of the class.
* Define a public static operation (getInstance()) that returns the sole instance of the class.

## If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

There is nothing in the heck called a middleware system on the internet. If I want to build a middleware, I will create a module package with multiple middlewares for the application construction. Then I import these packages into the different modules where I write code for routes and handlers and use them inside the router modules.

## Explain how the Singleton pattern can be used with Node modules, specifically with classes

We first create the class we want to be a singleton. Then, we instantiate an object of the same class in the class as a property. We then add a method to get back this instance, and we also add some logic that if the user tries to create another instance, never to do it.

```javascript

class PrivateSingleton {
    constructor() {
        this.message = 'I am an instance';
    }
}
class Singleton {
    constructor() {
        throw new Error('Use Singleton.getInstance()');
    }
    static getInstance() {
        if (!Singleton.instance) {
            Singleton.instance = new PrivateSingleton();
        }
        return Singleton.instance;
    }
}
module.exports = Singleton;

```

## Terms

### Router Middleware

It is a middleware that is applied to all methods done on a specific router object. Changes will apply each time the route is called by the user, modifying the requests.

### Dynamic Module Loading

Dynamic loading is a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory. Applications can still operate and run without these dependencies or modules, and they are only imported and injected into the application when only needed.

### Singleton Pattern

A singleton is a software engineering design pattern that uses the single instance of a class to control the instantiation of objects from the class.
We can't create more than one instance of the class, and all programming operations done by the class are managed through this single instance.

### CRUD -> REST Method Matches

It is the process when we match the HTTP request verbs with the corresponding database method done on data. So we have a GET request to read, a POST request to write, an UPDATE request to modify, a DELETE request to delete data from the database, and so on.

### Mock Testing

It is a way to perform unit tests for functions that require specific operations before and after they are called. We mock some functions to eliminate the logging effect to the console so it won't be crowded with unnecessary messages. There are many uses for mock tests, like using it to test server routes without having the server run on a specific port.
