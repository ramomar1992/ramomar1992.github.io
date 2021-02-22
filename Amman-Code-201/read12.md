# Canvas and Chart.js

## What is canvas?

\<canvas> is an HTML element, kind of similar to \<img>, but it has a closing \</canvas> tag and it does not have `alt:`attribute. It is used to draw shapes, charts, diagrams, or anything that has context. The \<canvas> element has attributes to control its width and height, which are the most important because without specifying these two attributes, the draw will be ruined.

### Basic usage of canvas

All major browsers support the canvas element, although older ones like IE8 or earlier don't. Therefore, we need to add a fallback code so if the user is still using these browsers, and they will still see an alternative. Also, the canvas methods can include a statement to check the users' rendering capabilities and write a fallback code to support them.

```html
<canvas id="stockGraph" width="150" height="150">
  current stock price: $3.15 + 0.15
</canvas>

<canvas id="clock" width="150" height="150">
  <img src="images/clock.png" width="150" height="150" alt=""/>
</canvas>

```


When adding a canvas element, we have to give it an ID attribute to be easy on javascript to recognize the element. Then, we need to give it a context, which is a method that accepts only one value that gives the element the basement to draw shapes and other things. Many different values could go inside the method, but the most basic one is 2d, which allows us to draw two dimensions. We also can check for the support and add a fallback code to check availability. \<canvas> also takes border, margin, and padding, and it is a good idea to style it using them.

```javascript

var canvas = document.getElementById('tutorial');

if (canvas.getContext) {
  var ctx = canvas.getContext('2d');
  // drawing code here
} else {
  // canvas-unsupported code here
}

```

Suppose we don't provide information to the canvas element that tells it what to draw. In that case, the result will be an empty, transparent box occupying the area of size we previously specified. To give information to the element, we add them to the context element using different methods; `fillStyle` and `fillShape`.

```javascript

    var ctx = canvas.getContext('2d');
    ctx.fillStyle = 'rgb(200, 0, 0)';
    ctx.fillRect(10, 10, 50, 50);
    ctx.fillStyle = 'rgba(0, 0, 200, 0.5)';
    ctx.fillRect(30, 30, 50, 50);
    

```

![image illustrate the shapes resulted from the above code](../images/Untitled.png)

### Drawing shapes with canvas

Before we begin drawing shapes like arcs, lines, triangles, and curves, we need to know about the canvas element's grid. We need to know that its origin begins from the top left corner. Each unit in the grid represents one pixel on the actual rendering. 

There are two basic drawings on canvas, which are rectangles and line paths. All other shapes must be drawn using a combination of paths. 

* #### Drawing Rectangles

To draw a rectangle, there are three functions:

1. fillRect(X,X,width,height) Draws a filled rectangle.
2. strokeRect(X,X,width,height) Draws a rectangular outline.
3. clearRect(x, y, width, height) Clears the specified rectangular area, making it fully transparent.

The x and y represent the origin top left corner of the rectangle. The width and height are for the size of the rectangle.

```javascript

function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.fillRect(25, 25, 100, 100);
    ctx.clearRect(45, 45, 60, 60);
    ctx.strokeRect(50, 50, 50, 50);
  }
}

```

* #### Drawing paths

They are a group of dots with a line through them. It can be straight or curve and have colors and different widths. To draw a path, we need to begin the path then specify with the `moteTo` method the starting point, which tells the browser where to begin drawing. It takes x and y coordinates that represent the distance from the origin top left corner. Then we can use different functions to draw the path.

1. beginPath(); Creates a new path.
2. moveTo(x,y); Moves the pen to the coordinates specified by x and y.
3. lineTo(x,y); Draws a line from the current drawing position to the position specified by x and y.
4. closePath(); Adds a straight line to the path, going to the start of the current sub-path.
5. stroke(); Draws the shape by stroking its outline.
6. fill(); Draws a solid shape by filling the path's content area.
7. arc(x, y, radius, startAngle, endAngle, anticlockwise); Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at endAngle going in the given direction indicated by anticlockwise (defaulting to clockwise).
8. arcTo(x1, y1, x2, y2, radius); Draws an arc with the given control points and radius, connected to the previous point by a straight line.
9. quadraticCurveTo(cp1x, cp1y, x, y) Draws a quadratic Bézier curve from the current pen position to the endpoint specified by x and y, using the control point specified by cp1x and cp1y.
10. bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y) Draws a cubic Bézier curve from the current pen position to the endpoint specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).
11. rect(x, y, width, height) Draws a rectangle whose top-left corner is specified by (x, y) with the specified width and height.

```javascript
// this code draws ttiangle
function draw() {
  var canvas = document.getElementById('canvas');
  if (canvas.getContext) {
    var ctx = canvas.getContext('2d');

    ctx.beginPath();
    ctx.moveTo(75, 50);
    ctx.lineTo(100, 75);
    ctx.lineTo(100, 25);
    ctx.fill();
  }
}

```

* ### Applying styles and colors

If we want to apply colors to a shape, there are two important properties we can use: fillStyle and strokeStyle.

* fillStyle = color; Sets the style used when filling shapes.
* strokeStyle = color; Sets the style for shapes' outlines.

We can also change the obacity of the coulor whether using RGBA colors or using this method:

`globalAlpha = transparencyValue;` Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.

We can apply different line styles using there properties: 

* lineWidth = value; Sets the width of lines drawn in the future.
* lineCap = type; Sets the appearance of the ends of lines.
* lineJoin = type; Sets the appearance of the "corners" where lines meet.
* miterLimit = value; Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
* getLineDash(); Returns the current line dash pattern array containing an even number of non-negative numbers.
* setLineDash(segments); Sets the current line dash pattern.
* lineDashOffset = value; Specifies where to start a dash array on a line.