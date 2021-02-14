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

## Document Object Model - DOM

DOM is the model of how JavaScript interacts with the web page. It is implemented by the browser and it covers two main features:

1. Making a model of the HTML page, and it is done by the DOM Tree method.
2. Accessing and changing the content. People call it the API which is an accronym to Application Programming Interface, and it is the underlying structure to how humen unteract with the model and change the HTML and what the visitor sees on the browser.

### DOM tree

The browser create a model of the page using the DOM tree and store it in the browser memory. DOM tree consists of four main nodes:

1. THE DOCUMENT NODE: document node is added on top of the Tree and it represnt the whole page. It is liek the first gate to the entire tree and if you want to access any of the page content you need to do that through the document node.
2. ELEMENT NODES: it describes the structure of the HTML and elements added on the page one by one. Through this node you can then access the text and the attribute nodes of an element. Relationships between the document and all of the element nodes are described using the same terms as a family tree: parents, children, siblings, ancestors, and descendants. (Every node is a descendant of the document node.)
3. ATTRIBUTE NODES: in the opening tag of any HTNL element there are attributes you can access and modify using scripts. They are considered part of the element not childrens of it.
4. TEXT NODES:  we can access the text of any element useing the text node. Any element inside the node are not considered a children of the text node but rather a childen of the element node.

### Working with DOM tree

To access the DOM tree, you need to do two main steps:

1. Locate and access the node the element in.
2. Use functions and methods to modify or change its content ot child elements or attribute.

#### Accessing elements

We can either select the element using DOM Quities or Traversing

##### DOM Quiryes

We can also select either individual element or group of elements.

###### Selecting individual element

Here are three common ways to select an individual element:

1. getElementByld()
2. querySelector()

###### Selecting group element

There are three common ways to select multiple elements.

1. getElementsByClassName()
2. getElementsByTagName()
3. querySelectorAll()

##### Traversing

You can move from one element node to a related element node.

1. parentNode
2. previousSibl ing / nextSibl ing
3. firstChild / lastChild

#### Working with the elements

Here is an overview of methods and properties that work with the elements

1. ACCESS/ UPDATE TEXT NODES
2. WORK WITH HTML CONTENT
3. ACCESS OR UPDATE ATTRIBUTE VALUES


