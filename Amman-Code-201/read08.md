# CSS Layouts

When designing a web page, it is different from designing a page to print or a poster to anything else. Web pages are flexible and can grow and shrink according to the screen's size. Therefore, when designing your web page, you have to know the core principles for positioning and layout your element on the screen to appear the same way you intended before publishing your website on all kinds of devices. Let us start with the first core concept:

## Blook and Inline

To understand HTML's elements, we have to sort them according to how these elements appear on a wen page. They can appear either on a block-level, meaning that they take a new line and take the whole screen width. You can control the width and height of this kind of element.
Examples: p, h1, h2, div, ul, ol, and li.

The second type is Inline level elements. These elements appear on the same line as the previous content, and they only take the width of their content. However, unlike block elements, inline elements must be converted to different display types to change their size.
Examples: a, img, label, button, em, and strong.

## Containing elements

We inevitably enclose groups of elements inside divs, so it will be easier for you to position them. When you put a group of elements inside a div or other block-level element, the outer container is called the parent element.

## Positions

In CSS, There are five positioning schemes:

### Static

Static is the most basic one. It positions the elements as they originally would appear if no CSS positioning applied to the page, as to how would HTML position page elements on top of one another. Every block-level element appears on a new line pushing all other elements underneath it down.

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

### Relative

Relative positioning does not take the element out of the normal flow. Thus element still holds its position on the page, but you can reposition the element relative to its previous position inside the containing. If you moved an element to flow over other elements, it would overlap with other elements without affecting their original position.

Note: To position the element after you change the position property, you can use the offset properties to change the element's position on the screen. Offset are: top, bottom, left, right.

```css
/* This code was taken from Duckett CSS book */

p.example {
position: relative;
top: 10px;
left: 100px;}

```

### Absolute

Absolute positioned elements are taken out from the normal flow. These elements are sitting in relation to their containing parent. Since they are out of the flow, they do not affect other elements' position. Still, the element's position on the page is taken out, allowing other elements to sit in their original position.

```css
/* This code was taken from Duckett CSS book */

h1 {
position: absolute;
top: 0px;
left: 500px;
width: 250px;}
p {
width: 450px;}

```

### fixed

Elements with float position do not affect other elements, and they do not move if the user scrolls the page. They are taken from the normal flow so that all elements can move around them and overlap.

```css
/* This code was taken from Duckett CSS book */

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

### Float

Floating an element allows you to take that element in normal flow and position it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

```css
/* This code was taken from Duckett CSS book */

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

### z-index

When elements are taken from the normal flow, they can overlap over each other. Therefore, you can specify the `z-index` property to determine which element should sit on top of the other.

### Using float position to create side-by-side design

In old designs, designers used the float positioning scheme to sit elements side-by-side, but they faced many problems with this property:

#### Elements blocking each other from sitting in the right place

When using float position on an element, its height affects where the following elements sit. Thus, it can also prevent certain elements from floating across the page to the desired side.

The designer solved this problem with another property; clear. Clearing the Float means clearing either side of the element from touching other elements. By setting its value to Right, you prevent elements from touching it from the right, and if it is set to Left or Both, you prevent the left or both sides to touch other adjacent elements, respectively.

```css
/* This code was taken from Duckett CSS book */

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

This problem emerged when developers created parent blocks containing elements in which all are set to float. The browser then gives the parent a height of zero, and its top and bottom borders are combined in one thick line on either side.

Programmers tended to add another non-floating element inside the containing block with clear property sit to both. But, this approach seemed redundant since it means adding an extra element to the HTML. Therefore, they create another CSS solution. We set its width to 100% and the overflow property to auto for boxes with all elements as Float.

```css
/* This code was taken from Duckett CSS book */

div {
border: 1px solid #665544;
overflow: auto;
width: 100%;}

```

### Creating multi-column layout

If you want to create a page that contains multiple columns in the layout, you must use three properties: Float, width, and margin.
You first need to sit all elements inside \<div> elements. Then you apply these three properties to the div itself, not the same elements. The width is to specify how wide the div should appear. The Float is to sit the position of the div to float around the page. Last, the margin property sits to determine the distance between the columns.

```css

.column1of2 {
float: left;
width: 620px;
margin: 10px;}
.column2of2 {
float: left;
width: 300px;
margin: 10px;}

```

## Screen Size, Resolution, and Layouts

Different screens have different screen sizes and resolutions. Some screens have wider measures than others; therefore, this issue becomes a headache to the web designer. They usually create their design on 960-1000 pixels wide and 560 pixels long. Yet, these days, users may use the web on TVs, laptops, computer screens, tablets, or mobile phones. So, screen contents and elements would appear different according to each screen size of these devices.

Nowadays, designers created the flexible-layout design or the responsive design with which a web page can adjust its size, and the web page will still appear neat regardless of the screen size a user might have.

### A fixed  layout

This design has many advantages; that is, it created more space for the designer to lay elements more accurately since they tend to use pixels for measures. It enabled them to control line size and image size and keep them relative to the rest of the web page element. 

However, it also contains many disadvantages. The most obvious one is that the page does not appear nice on smaller or larger screen sizes. So, if the user screen resolution is higher than the designer screen resolution, the lines will appear too small, making them very hard to read and vice versa. Besides, if the user changes their font size, the text might appear bigger or smaller, making it hard to read. Also, with this design, pages tend to take up more vertical space than liquid designs.

### A liquid layout

This design appears to look more screen size-friendly since designers use percentages instead of pixels. Pages designed using the layout will stretch to take the screen's whole width, and if the user has a smaller screen, they will adapt to the new size. The page can tolerate the sitting a user may sit for the font size, making them easier to read.

On the other hand, this design has these cons. First, if the user has a very large screen, the font will appear too big since it can stretch, creating harder text to read. It can create some problem with fixed-width elements like images and inconsistent with the rest of the page elements.

## Grid Layouts

Using a grid to layout the content on a web page is very common among web designers. It is a very advanced way to show a professional web page and consistency between element and content, and it has so many benefits:

* Creates a continuity between different pages
* Helps users predict where to find information on various pages
* Makes it easier to add new content to the site in a consistent way
* Helps people collaborate on the design of a site in a consistent way

### 12 Colomns, 960 Pixles Grid

It is the most common grid. The page is 960 pixels wide, and there are 12 equal sized columns, each of which is is 60 pixels wide. Each column has a margin set to 10 pixels, which creates a gap of 20 pixels between each column and 10 pixels to the left and right-hand sides of the page.

![Image shows an example of a grid layout](/images/gridLayout.png) ![Image shows an example of a grid layout](/images/gridLayout2.png)

### CSS Frameworks

CSS frameworks are tools that make coding easier since they provide a pre-written code that you can use for your page, such as creating layout grids, styling forms, creating printer-friendly versions of pages, and others. They save you time from writing code for the same task repeatedly, and they are tested among a wide range of devices and users, so they work very well on any device. On the other hand, they have more code than needed that you might add to your page unintentionally, as well as they require you to add classes to your HTML code that is for design purposes and is not descriptive.

### Multiple style sheets

Some web designers decide to split their style sheets into more than one file to have one sheet that controls the font color and font family and the font's color and another one to control the layout and how the element should be positioned on the page and so on.

We can use this approach by linking more than one style sheet file to the same HTML in two ways, whether we can add a new link element to the head of the HTML or add the sheet URL to the CSS file already linked to our HTML page.

```css

@import url("tables.css");
@import url("typography.css");
body {
color: #666666;
background-color: #f8f8f8;
text-align: center;}
#page {
width: 600px;
text-align: left;
margin-left: auto;
margin-right: auto;
border: 1px solid #d6d6d6;
padding: 20px;}
h3 {
color: #547ca0;}

```
