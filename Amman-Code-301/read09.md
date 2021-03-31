# Functional Programming

It is a programming paradigm or style that programmers follow to write code characterized by being readable and maintainable. Writing functional code reduces the overhead of maintenance and allows us to write side-effect-free functions.

## Pure functions

For a function to be pure, it should always return the same result for the same parameters. Functions that rely on global objects in the processing are not considered a pure function because global objects might change at any time of the runtime, either intentionally by the user or by the program itself.

Characteristics of pure functions:

* Return the same value if given the same parameters over and over.
* Do not cause any side effects.

### What makes a function impure because of returning different values for the same arguments

* If it relies on a global object that was not passed as an argument. To solve this issue, we have to add a new parameter and pass that global object inside the arguments list.
* If the function reads external files.
* If the returned value relies on a random number generator.

### What makes a function impure with side effects

* If it modifies a global object.
* if it modifies objects passed by reference

Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. Functions should be isolated and unable to change any other parts of the program.

The most significant benefit of writing pure function is that it is way easier to test the code.

## Immutability

The second characteristic of functional programming is immutability, which means not change any part of the system during runtime. To attain immutability, we have to adopt two main concepts when writing code:

1. Recursive functions
2. Chaining methods

## Referential transparency

For a function to be Referentialy transparent, it must be pure and return consistent values to use this function result to initialize another function. What we try to achieve from this is to make a new function call by passing a call to the same function as an argument in the parameter list, so the returned value from the evaluation of the function will be an argument to the next function call.

## Functions as first-class entities

The idea of functions as first-class entities is that functions are also treated as values and used as data.

Functions as first-class entities can:

* Refer to it from constants and variables
* Pass it as a parameter to other functions
* Return it as a result of other functions

The idea is to treat functions as values and pass functions like data. This way, we can combine different functions to create new functions with new behavior.

### Higher-order functions

Higher-order functions are functions that either:

* Take one or more functions as arguments
* Return a function as its result