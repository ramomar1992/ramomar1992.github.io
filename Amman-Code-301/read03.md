# MUSTACHE and FLEXBOX

## MUSTACHE

It is a templating specification that allows us to separate data from representation. The template is HTML markups populated with tags that could be variables or programming logic. These tags are then replaced with actual data at runtime, and then the template will be rendered in HTML. It does not use if statements or loops or any other kind of logic.

The mustache.js is a Javascript representation of the mustache templating syntax that allows us to use the template to render a client-side website without implementing it on the server.

Mustache.js syntax is very simple. We only need to wrap the place holder into a double set of curly braces `{{name}}`. The name is a property placeholder that, when at runtime, it will be replaced with the actual value and show in the HTML markup.

```javascript
var view = {
  title: "Joe",
  calc: function () {
    return 2 + 4;
  }
};

var output = Mustache.render("{{title}} spends {{calc}}", view);

```

Notice that the function takes two params. The first is a template populated with mustache tags. The second is an object with a property with the same name as the tag names inside the template. The names are HTML escaped. If you wish to use unescaped names, use a triple set of curlies or the amp sign '&'.

## FlexBox

Flexbox is a CSS layout technique that gives us full control over the space inside any container with element residing in it. It controls how elements are spaced out inside the containing box and their layout. It also controls what happens to the element and the box when the elements' size increases or shrinks to prevent overflow.

### Terminology

- Flex container: is the parent box that holds the elements.
- Flex items: are the elements that reside inside the container.
- Flex-flow direction: The direction that elements inside the parent container flow with to lay themselves out.
- Main axis: if the main direction of the elements' flow. It has main-start and main-end positions according to the flow, if it was normal or reverse. It defaults to row, which is the X-axis of the container element. It has a  main-size property which is the height or the width of the container depending on the flow direction.
- Cross axis: is the perpendicular direction of the main axis. It has cross-start and cross-end positions according to the flow, if it was normal or reverse. It defaults to the Y-axis of the container element. It has a cross-size property that is the height or width of the container and depends on the direction of the flow.

### Flex properties

1. Container element properties:

   - `display`: which should be set to `flex;`
   - `flex-direction`: which is set to on of these four values: `row;`,`row-reverse;`,`column;`, and `column-reverse;`.
   - `flex-wrap`: may take one of three values: `wrap;`, `wrap-reverse;`, and `no-wrap;`.
   - `flex-flow`: which can take the flex direction and flex wrap values in order, this is a shorthand property to them.
   - `justify-content`: may take one of these values: `flex-end;`, `flex-start;` the default, `center;`, `left;`, `right;`, `space-between;`, `space-evenly;`, `space-around;`, `safe;`, and `unsafe;`.
   - `align-items`: it may take one of these values: `stretch;` the default, `flex-start;`, `flex-end;`, `center;` and `baseline;`.
   - `align-content`: which takes one of these values: `center;`, `flex-end;`, `flex-start;`, `space-between;`, `space-around;`, `space-evenly;`, and `stretch;`.

2. Properties for the Children

    - `order`: which may take any integer to order elements. 
    - `flex-grow`: takes a number. To fill the rest of the available space on the main axis.
    - `flex-shrink`: takes a number. Controls how elements shrink when there is no space available.
    - `flex-basis`: takes a size measure. Control the size of the element before the remaining space is distributed. It overrides the width and min-width properties.
    - `flex`: a shorthand that takes the grow, shrink, and basis flex rules in order.
    - `align-self`: this allows to override the normal alignment of an individual element. 