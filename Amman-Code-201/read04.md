# HTML Links - CSS Layouts - JavaScript Functions, Methods, and Objects

## HTML Links

## CSS Layouts

When we take about designing a web page, it is different than designing a page to print or a poster ot any thing else. Web pages are flexible and can grow and shrink according to the screen's size. Therefore, when designing your web page, you have to know the core principles for positioning and layout your element on the  screen to appear the same way you intended before publishing your web site on all kind of devices. Lets start with first core concept:

### Blook and Inline 

To understand HTML's elements, we have to sort them acoording to how these elements appear on a wen page. They can appear either on a block level; meaning that they take new line and take the whole width if the screen. You can control the width and height of this kind of element.
Examples: p, h1, h2, div, ul, ol, and li.

The second type is Inline level elements. This kind of elements appear on the same line as the previous content, and they only take the width of thier content. However, unlike block elements, inline elements must be converted to different dysplay type to change their size.
Examples: a , img, label, button, em , and strong.

### Containing elements

It is inevatable to enclose groups of elements inside divs so it will be easier for you to position them. When you put a group of elements inside a div or other block level element, the outer container is called the parent element.

### Positions

In CSS, There are five poisioning schemes:

#### Static:

Static is the most basic one and it positions the elements as they originally would appear if no CSS positioning applied to the page; as how would HTML position page elements on top of one another. Every block level element appear on a new line pushing all other elements underneath it down.

```css
/* this code was taken form Duckatt CSS book */
body {
width: 750px;
font-family: Arial, Verdana, sans-serif;
color: #665544;}
h1 {
position: static;
background-color: #efefef;
padding: 10px;}
p {
position: static;
width: 450px;}

```

#### Relative

Realtive positioning does not take the element out of the normal flow, thus element still holds its position on the page, but you can repositoion the element relative to its previous position inside the containing. If you moved an element so it can overflow on other elements, it would overlap with other elements without affecting their original position.

Note: To position element after you change the position property, you can use the offset properties to change the element's poition on the screen. Offset are: top, bottom, left, right.

```css
/* this code was taken form Duckatt CSS book */

p.example {
position: relative;
top: 10px;
left: 100px;}

```

#### Absolute

Absolute positioned element are taken out from the normal flow. These elements are sitting in relation to their containing parent. Since they are out of the flow, they do not affect other elements position, but the element's own position on the page is taken out allowing other elements to sit on its originial position.

```css
/* this code was taken form Duckatt CSS book */

h1 {
position: absolute;
top: 0px;
left: 500px;
width: 250px;}
p {
width: 450px;}

```


#### fixed

Elements with float position do not affect other elements and they do not move if the user scroll the page. They are taken from the normal flow, so all elements can move around them and can overlap with them.

```css
/* this code was taken form Duckatt CSS book */

h1 {
position: fixed;
top: 0px;
left: 50px;
padding: 10px;
margin: 0px;
width: 100%;
background-color: #efefef;}
p.example {
margin-top: 100px;}

```

#### Float

Floating an element allows you to take that element in normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

```css
/* this code was taken form Duckatt CSS book */

blockquote {
float: right;
width: 275px;
font-size: 130%;
font-style: italic;
font-family: Georgia, Times, serif;
margin: 0px 0px 10px 10px;
padding: 10px;
border-top: 1px solid #665544;
border-bottom: 1px solid #665544;}

```

Note: When elements are taken from the normal flow, they can overlap over each other. Therefore, you can specify the z-index to determain which element should sit on top of the other.

### Using float poition to create side-by-side design

In old designs, designers used float to sit elements side-by-side, but they faced many problems with thos property:

#### Eements blocking each other from sitting in the right place

When using float on element, its height affects where the following elements sit. Thus, it can also prevent certein element from floting across the pahe to the desired side.

Designer solved this problem with another property; clear. Clearing the float means to clear either side of the element from touching other elements. By sitting its value to right, you prevent elements to touch it from the right, and if it is sit to left or both you prevent the left or both sides to touch other adjacent elements respectively.

```css
/* this code was taken form Duckatt CSS book */

body {
width: 750px;
font-family: Arial, Verdana, sans-serif;
color: #665544;}
p {
width: 230px;
float: left;
margin: 5px;
padding: 5px;
background-color: #efefef;}
p.clear {
clear: left;}

```

#### Containing box height is set to zero

This problem emerged when developers creared parent blocks containing elements in which all are set to float. The browser then gives the parent a height of zero, and its top and bottom borders are combind together in one thick line on either sides. 

Programmers tended to add another non-floating element inside the containing block with clear property sit to both. But, this approach seemed redundant since it means to add extra element the HTML. Therefore, they create another CSS solution. For boxes that have all elements as float, we sit its width to 100% and the overlow property to auto.

```css
/* this code was taken form Duckatt CSS book */

div {
border: 1px solid #665544;
overflow: auto;
width: 100%;}

```

## JavaScript Functions, Methods, and Objects
