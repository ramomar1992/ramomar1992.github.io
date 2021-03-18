# RESPONSIVE WEB DESIGN and FLOATS

## RESPONSIVE WEB DESIGN

The term responsive web design was invented in the early 2010s to resolve the problem with the increasing number of people who browse the web using their mobile devices. There was a need to make websites adaptive and capable of being rendered on mobile devices properly without losing the user experience or any details desktop websites provide. 

### Mobile websites

Some companies make a separate mobile website with a separate domain name. Although this approach makes the website liter and faster to load, it wasn't a great solution. A new domain means a new codebase with different dependencies, which was not convenient for users or developers.

### Responsive and Adaptive websites

Responsive websites can change rapidly in response to any change—while adaptive means to fluidly modify state to suit a new purpose. When we combine these two approaches, we can reach for the best user experience on any device regardless of the screen width or any other factor.

Responsive and Adaptive websites' ideas are attained through three main concepts: Flexible Layouts, Media Queries, and Flexible Media.

#### Flixible layout

It is the practice of building a flexible grid that is adaptive to all screen sizes and widths. It includes using relative units like percentages and em to lay components out on screen, not absolute values. This will make the page changes dynamically to any modification in screen size.

New units are used:

* vh: veiwport hieght
* vw: veiwport width
* vmin: minimum viewport height or width
* vmax: maximum viewport height or width

To help calculate the fixed value proportions, we can use this formula: result=  target ÷ context.

#### Media Queries

We can specify a complete style to a web page when certain circumstances are met using media queries. We add different conditions the browser checks; if all these conditions are met, the page's style will apply the style sheet that corresponds to them. There are three ways to declare media queries. 

1. Link to the sheets from the HTML file. `<link href="styles.css" rel="stylesheet" media="all and (max-width: 1024px)">`
2. Using the @media rule in the style sheet. `@media all and (max-width: 1024px) {...}`
3. Using the @import rule in the style sheet. `@import url(styles.css) all and (max-width: 1024px) {...}`

Each media query may include media type and conditions. If the media type were not specified, it would default to `screen`. Other media type like `tv` , `print`, `all` , `braille` and others. 

Three logical operators help us write powerful expressions: and, not, only in addition to comma, which act like an or operator to help us select more queries.

Media features:

1. Height & Width Media Features `@media all and (min-width: 320px) and (max-width: 780px) {...}`
2. Orientation Media Feature `@media all and (orientation: landscape) {...}`
3. Aspect Ratio Media Features `@media all and (min-device-aspect-ratio: 16/9) {...}`
4. Pixel Ratio Media Features `@media only screen and (-webkit-min-device-pixel-ratio: 1.3), only screen and (min-device-pixel-ratio: 1.3) {...}`
5. Resolution Media Feature `@media print and (min-resolution: 300dpi) {...}`

#### Flexible Media

When we want to add media to the website, we have to give it a relative width size to scale relative to the screen width and orientation.
For embedded media like YouTube videos, we need to place the iframe tag inside a parent element, say a div. Then we have to make it width 100% with height equals to zero. We need to give it padding-bottom with a percentage equal to the result of the video's dividing aspect ratio. Last, we need to set the position to relative. We have to set the media tag height and width to 100% for the media tag and position it as absolute by fixing it to the top left corner of the parent element.

### Mobile First

It is an approach that compels developers to start their design with mobile phone design then add media queries to the bigger screen size devices. This was invented to keep mobile device users in mind when developers are working in the production. It also saves the bandwidth that the phone might waste when loading desktop websites design then load mobile media queries.

#### Float

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

Note: When elements are taken from the normal flow, they can overlap over each other. Therefore, you can specify the z-index to determine which element should sit on top of the other.

### Using float position to create side-by-side design

In old designs, designers used the float positioning scheme to sit elements side-by-side, but they faced many problems with this property:

#### Elements blocking each other from sitting in the right place

When using float position on an element, its height affects where the following elements sit. Thus, it can also prevent certain elements from floating across the page to the desired side.

The designer solved this problem with another property; clear. Clearing the Float means clearing either side of the element from touching other elements. By setting its value to Right, you prevent elements from touching it from the right, and if it is set to Left or Both, you prevent the left or both sides to touch other adjacent elements, respectively.

```css

p {
width: 230px;
float: left;
margin: 5px;
padding: 5px;
background-color: #efefef;
clear: left;
}

```

#### Containing box height is set to zero

This problem emerged when developers created parent blocks containing elements in which all are set to float. The browser then gives the parent a height of zero, and its top and bottom borders are combined in one thick line on either side.

Programmers tended to add another non-floating element inside the containing block with clear property sit to both. But, this approach seemed redundant since it means adding an extra element to the HTML. Therefore, they create another CSS solution. We set its width to 100% and the overflow property to auto for boxes with all elements as Float.

```css
/* This code was taken from Duckett CSS book */

div {
overflow: auto;
width: 100%;}

```

Or better, we can use the `:after` meta tag:

```css

.clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;
}

```
