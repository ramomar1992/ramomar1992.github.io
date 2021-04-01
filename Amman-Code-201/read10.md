# JavaScript - Error Handling and Debugging

No one writes code with no mistakes or errors, even the best programmers on earth. Therefore, there are special tools that programmers can use to trace their code line by line and fix these errors. We usually call them *BUGS*, and the tool that provides us with the functionality to correct them is called *DECUGGER*.

## Order of Execution and Execution Contexts

JavaScript interpreter does not read the code as numbered by line. If some tasks need to wait until others are finished, it will hold the control of that task and move it to the task it needs to be finished, and then it will come back to the previous one.

Moreover, JavaScript uses the concept of scopes and execution context. This means that when a new function is being called anywhere in the script while the execution reaches the function, a new context will be created to execute it. This is similar to the Stack Records in C and C++. There is two main execution context in the language:

1. Global Context: it is when the code being run is outside all functions.
2. Function Context: it is when the code being run is inside the function

Variables, in turn, have their own scopes according to where they are declared in the script. The Global Scope variables are the ones that are declared globally, and they are available to use anywhere in the script, even inside functions. Function Scope variables are variables declared inside functions, and once the function is terminated, they become invalid to use outside the function.

## Hoisting

When each context is created to be executed, variables and functions are declared first. Therefore, we can write in our code functions and variables used before their declarations.

These are the two phases that happen when any execution context activates:

1. Prepare phase: it is when the new scope is created, and all variables, functions, and arguments are created as well as determining the THIS keyword value.
2. Execute phase: in this phase, variables are assigned, functions are referenced, and their code is executed.

When we understand these two phases, we realize that no matter where you declare functions and variables since they are created before executing phase, the control will see them first and go to the statements where they are used.

When execution context is created, a new variables object that holds all variables in the context will also be created. This object is inaccessible by the user. Note that parent context can not access variables inside children's variables object; in contrast, children can reach to their parent variables and use them although it is costly in performance.

## Errors

Interpreters are smart enough to see errors, so they stop the code and look for error handling code when they see errors. If the interpreter finds the code to handle the error, it will use the code and continue the execution normally; Otherwise, it will look in the outer scope, which could be the function in which it was called. If there is no error handling code in any of the functions called it, it continues looking for it in the contexts that lead to its execution until it reaches the global scope, where it will throw an exception and terminate the script.

There are seven types of built-in error objects in JavaScript:

![Error Objects](../images/ErrorObject.jpg)

## Error Objects

Error objects can help you find where your mistakes are and browsers have tools to help you read them. When an Error object is created, it will contain the following properties:

![Error Properties](../images/ErrorProperties.jpg)
