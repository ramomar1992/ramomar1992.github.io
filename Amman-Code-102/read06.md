# CSS - Cascading Style Sheets

It is a designing directions to tell HTML pages how to display their elements. It is used to add "style" to the web page in differnt way. Its main features are:

1. Positioning.
2. Reizing.
3. Coloring.
4. Aligning.

These are the main concept for what CSS originally created. There are also other useful functions and capabilities that CSS can add to web pages.

## How to write CSS code:
There are three ways to how we write CSS code. Whether we can write it inline, internal, or external.

### Inline CSS
By adding the style attribute to any HTML tag and changeing properties inside the value of the attributes we can add css styling on that particuler tag:
```html
    <h1 style="color:red;"> Any text </h1>
```
in the previous code, the ``` color:red;``` inside the style tage is an inline css command. It tells the heading tag to change its text color to red.
Although we can still write inline css and browsers do not complain about it, it is now considered bad practice and we have to write css outside HTML tags.

### Internal CSS

We can add a special \<style\> tag inside the head of the HTML page, and then we add css between the openning and the closing tag. We first have to selet the element or the group of elements that we want to change its style properties, and add the name of the property inside a set of curly braces separated by semi-colons. We write the value of the property after we add a colon between the  value and the name:
```html
    <html>
        <head>
            <style>
                h1{
                    color:red;
                    background-color: blue;
                }
            </style>
        </head>
    </html>


```
This way of writing the code inside the head is not so acceptable. Unless you have a one page web site do not use this approach. Css files should be separated from HTML files and this is the best practice.

### External CSS

The best practice to add CSS code to your HTML pages is by creating a separate file, most likely to be called styles.css. Notes the extension of the file .css, which refer to the code inside it. in the head of the HTML page we add a special self-closing tag called \<link\> inside the link we add three attriutes, *rel* its value should be **stylesheet** which tells the HTML what is the relation between the file we want to link to with our HTML file,  and the *href* which tells the HTML the location of the file, and last, the *type* attribute which tell the page what kind of files it is, most of the time we specify **text/css** as its value.



```html
    <html>
        <head>
            <link rel="stylesheet" href="some/location.css" type ="text/css" />
        </head>
    </html>


```
inside the css file we write the code just as we do if it was internal. Write the element selector, and inside a se of curlies we add the properties and their valuse separated by semi-colons.

```css

    h1 {
        color: red;
        background-color: blue;
    }
```


## CSS color systems:
In order to determaine colors to apply to your elements, there are different systems you can use:

* RGB system  ``` color: rgb (255 , 255 , 255)```
* Hexadicimal RGB system ``` color: #ffffff```
* HSL ``` color: hsl(650 , 0.123 , 20%)```
* HSL alpha  ``` color: hsl (560 , 0.563, 44%, 0.3)```
* RGB alpa ``` color: rgb (255, 255, 255, 1.0)```


# JavaScript Functions

Functions are pieces of codes that have a name and a special functions. The can have arguments as inputs and retuen values as output. The main purpose of functoins is, they make code easy reusable and easier to write. When we declare a function to calculate average student in each class at school, we just have to write the code for the operations inside the funcion once, and when we want to reuse that function again, we only have to call its name with parenthises. 

## How do we write functions

Functions have four essential parts:

* the function keyword 
* function name
* a list of parameters (can be empty)
* the code inside curlies (may contain return statement)
  
### Function declarations
This is one way to create a function :
``` javascript

    function funcName (param)
    {
        input;
        code;
        output;
        return something;
    }
```

When we call the function we call it by the dunction name that follows the function keyword directly.
```javascript

    funcName(args);
```
### Function expressions
The second way to write a function is, to assign the function to a variable:
```javascript

    var funcName = function(parameters) {
        input;
        code;
        output;
        return something;
    }

```
When we want to call the function we call it be the name of the variable followed by argument list inside parenthises and semi-colon

```javascript

    funcExpression(args);
```