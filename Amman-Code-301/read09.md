# Functional Programming

It is a programming paradigm or style that programmers follow to write code charecterized of being readable and maintainable. Writing functional code reduces the overhead of maintinance and allows us to write side-effect-free functions.

## Pure functions

For a function to be pure, it should always return the same result for the same parameters. Functions that rely on global objects in processing are not considered as pure function, because global ojects might change at any time of the runtime, either intentionally by the user or by the program itself.

Charectersitcs of pure functions:

* Return the same value if gived the same parameters over and over.
* Do not cause any side effects.

### What makes a function impure beacause of returnend different values for the same arguments

* If it relies on a global object that was not pass as an argument. To solve this issue, we have to add new parameter and pass that global object inside the arguments list.
* If the function reads external files.
* If the returned value relies on random number generator.

### What makes a function impure with side effecrs

* If it modifies a global object.
* if it modifies objects passed by reference

Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result. Functions should be isolated and unable to change any other parts of the program.

The most segnificent benefit of writing pure function is that it is way easier to test the code.

## Immutability

The second charecterstic of functional programming is immutability, which means to not cahnge any part of the system while runtime. To attain immutability we have to adopt two main concepts when writing code:

1. Recursive functions
2. Chaining methods

## Referential transparency

For a function to be Referentialy transparent, it must be pure and return consistent values, so we can use this function result to initialize another function. What we are trying to achieve from this, is to make a new function call by passing a call to the same function as an  arguent in the parameter list, so the returned value from evaluation the function will be an argument to the next function call.

## Functions as first-class entities

The idea of functions as first-class entities is that functions are also treated as values and used as data.

Functions as first-class entities can:

* Refer to it from constants and variables
* Ppass it as a parameter to other functions
* Return it as result from other functions

The idea is to treat functions as values and pass functions like data. This way we can combine different functions to create new functions with new behavior.

### Higher-order functions

Higher-order functions are functions that either:

* Ttake one or more functions as arguments
* Return a function as its result
