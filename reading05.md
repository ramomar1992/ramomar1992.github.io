# Logical Operators and Work Flow Statements
## <u>Logical operators:</u>

In JavaScript, there are three main logical operators that can be used in conditional checking; these are the logical AND(&&), the logical OR(\|\|), and the logical NOT(!). Each one of these operators works differently from the others. <br>

| A | B | A && b | A \|\| B | !A |
| --- | --- | --- | --- | --- |
| true | true | true | true | false |
| true | false | false | true | false |
| false | true | false | true | true |
| false | false | false | false | true |
  
## <u>Decicion Making and Loops:</u>

We, most of the time, won't build our application imperatively. There must be a work flow based on conditions, re-executing a particular block of code for a desired number of times, or continuing the running code based on the user's input and interaction with the web page.

Let's discover two fundamental concepts of programming. Conditions and Loops:

### <b><em>Conditional statements</em></b>:
Conditional statements are pieces of code that are run based on an evaluated condition inside the check. The code that is run after the evaluation depends on the returned result; if it was True, the execution transferred to the immediate block of code that follows. 
```javascript
if (condition){
    cond statements;
}

```
We can also add whatever conditions to be checked after the first block and have the main condition evaluated to False, the next one will be checked, and so on until the check returns true. 
```javascript
if (condition 2){
    cond statements 1;
} else if (condition 2) {
    cond statement 2;
}

```
In the end, if no condition returned True, we can choose to either add an Else statement, or we can leave the code to continue without executing any if statements. 
```javascript
if (condition 2){
    cond statements 1;
} else if (condition 2) {
    cond satement 2;
} else {
    statement when no True condition;
}

```

### <b><em>Loops:</em></b>

Suppose that we want to execute a particular code a specific number of times. Should we write the same code that many times? It looks that the code is going to be cluttered and hard to read. Besides, what if we want the user to determine how much that number will be? Then, we should think about all possible numbers and write code for it. In fact, this does not work like this. In programming, there is a concept looping, in which you give the computer the command to run a code the number of times you or the user might want.
There are three types of looping statements in JavaScript; For loop, While loop, and Do While loop.

The <strong><u>For</u></strong> loop is used when you know exactly how many times you want to loop. The sentence contains three parts; a declaration, a condition, and an update statements. We start by declaring a variable that will be our initial value to start the loop. A condition is then checked against this value in which the loop will continue looping until this condition fails. 

```javascript
 for ( declaration ; condition; update ){
     statemets to execute;
 }

```
<strong><u>While</u></strong> loop is used when you do not know the number of times to loop through the code. In addition, you can use it for input checking when you expect the user to enter something like a password or a user name, as well as to check whether the date type entered is valed or not.
It starts by the keyword <em>While</em>, then you type the condition you want to check each time of looping followed by statements to execute.

```javascript
 while ( condition ){
     statemets to execute;
 }

```

Last but not lease, the <em>Do While loop</em>. This loop ensures that the code inside the loop will be executed at least one time. After that execution, the condition will check. If it was true it will continue looping until it fails.


```javascript
do{
    statements to execute;
} while ( condition );

```

