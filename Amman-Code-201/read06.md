# JavaScript Object and DOM

## Objects in JavaScript

Object is a collection of data that model a real world objects.
It cotains variables and functions encapsulted insdie one intitiy.
Variables inside the object are called properties, and functions are called methods.
Properties and methods are writen inside the object declarationa as keys and values.

### Creating objects leterals

We start declaring out object using the var key word and the name of the function, them we type the assignment operator, after that, we write the properties and method inside a set of curly braces.
The name of the functions and variables inside the object are called keys, Two keys can not have the same name because they will have conflict with the value they hold.

```javascript

let obj ={
    key1: 'value',
    key2: 123,
    key4: true,
    key5: ['values', 'in', 'an', 'array'],
    method1: function(){
        do something;
    }   

};

```

There a special keyword used inside functions; the This keyword, We use to indicate the the object we want to fitch its properties is the same object; not other objects.

We can access the object's memebers useing the dot member operator or square brackets.

```javascript

let variable = obj.key1;
let variable2 = obj.method1();
let variable3 = obj['key4'];

```

### creating objects by construction notation

Another way to create the object is using object constructer nad the new keyword.
We declare the varible and assign it to `new Object();`. Then, we can add however many properties and methods to the object using the member operator. We can use this way to add properties and methods to objects created using leteral notationsas well.

```javascript

var obj = new Object();
object.key1 = 'Value1';
obj.key2 = 123;
obj.method1 = function(){
    do someething;
};
delete obj.key1;

```

You can change the object properties and call its methods using the dot operator.
You can delete the property or method using the delete keyword.

### Using functions to construct many objects

We can use the function constructor notation to create many object of the same template. 

```javascript

function obj (param1, param2, param3){
    this.key1 = param1;
    this.key2 = param2;
    this.key3 = param3;
    this.method1 = function(){
        do something;
    };
}

```

Notice that we created the function with uppercase, to remind the programmer that when they want to use the function constuctor they will remembet it is and object constructor not a regular function.

We can create instances of the object using the new keyword and the function name. Then we provide the arguments needed to create the instance of the object. This type of objects is needed when you have a complex script that require you to create object instances in different places but you do not know wehre yes.
