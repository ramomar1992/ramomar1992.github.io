# Data Modeling

## Name 3 advantages to Test Driven Development

1. Increase the workflow efficiency and decrease the error
2. Ensure continuous integration and code flexibility and easier maintenance
3. Better program design and higher code quality
4. TDD reduces the time required for project development

## In what case would you need to use beforeEach() or afterEach() in a test suite?

When there is a function that we need to use before each unit test, this function is used inside the functions that we are testing. `beforeEach()` and `afterEach()` handles the asynchronous calls.
When we want to mock functions that are likely to output data, that will make the output screen crowded. Also, some functions use some resources that will affect the program and the device's performance.

## What is one downside of Test Driven Development

* Tests can not find bugs that you simply introduce within the test code and the implementation code.
* Slow process
* All the members of a team got to do it
* Tests got to be maintained when requirements change

## What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?

Constructor functions are hoisted while classes are not.
The syntax. Classes use a special method called the constructor.

## Why REST?

One of the key advantages of REST APIs is that they provide a great deal of flexibility. Data is not tied to resources or methods, so REST can handle multiple types of calls, return different data formats and even change structurally with the correct implementation of hypermedia. This flexibility allows developers to build an API that meets your needs while also meeting the needs of very diverse customers.

* Developers like REST because the learning curve is less steep.
* Web Services contract-first approach is more complex.
* The footprint of SOAP is too big for mobile, while the REST footprint is small and can be used very easily as it is based on HTTP protocol.
* Parsing of JSON is less compute and memory intensive than XML.

REST is much easier than other approaches such as SOAP which keeps developers from reinventing the wheel as far as HTTP request operations go. SOAP also requires separate server and client programs.

Since REST is based on standard HTTP operations, it uses verbs with specific meanings such as "get" or "delete," which avoids ambiguity. Resources are assigned individual URIs, adding flexibility.

With REST, information produced and consumed is separated from the technologies that facilitate production and consumption. As a result, REST performs well, is highly scalable, simple, and easy to modify and extend.

## Terms

* Functional programming: the process of building software by composing pure functions, avoiding shared states, mutable data, and side effects.
* Object-oriented programming (OOP): a programming paradigm that relies on the concept of classes and objects. It is used to structure a software program into simple, reusable pieces of code blueprints (usually called classes), which are used to create individual instances of objects
* Class: classes are the building blocks of OOP. A class is a collection of data and methods representing a particular object and allowing us to create as many of that object as we want consistently and functionally.
* super: is the class from which the subclass has been derived. It is mainly a keyword used to initialize the parent object from the child object
* this: it is a keyword used in OOB that refers to the same object we work on.
* Test Driven Development (TDD): it is a programming style that requires programmers to use unit tests for each functionality in the program. It ensures the quality and the integration of the program.
* Jest: it is a package that allows us to perform the unit test on Node code.
* Continuous Integration (CI): the process of maintaining code with tests and refactoring to allow the integration of the new code in the previous code and ensure the readiness of deployment.
* REST: stands for Representational State Transfer. It is a software architectural style that uses a subset of HTTP. It is commonly used to create interactive applications that use Web services.
* Data Model: An abstract model that organizes data elements and standardizes how they relate to one another and the properties of real-world entities.

## Which three things had you heard about previously and now have better clarity on?

1. Testing with JEST
2. SQL languages
3. Databases

## Which three things are you hoping to learn more about in the upcoming lecture/demo?

1. NoSQL
2. MongoDB
3. MongoosAPI

## What are you most excited about trying to implement or see how it works?

An application that works utilizing MongoDB and NoSQL database.
