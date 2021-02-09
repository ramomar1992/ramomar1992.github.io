# HTML Lists, CSS Boxes, JS Control Flow

## HTML Lists

Sometimes on your web page, you want to use lists of items; therefore, HTML provides three types of lists that you can use:

### Ordered lists

To make this kind of list, you have to write \<ol> which stands for an ordered list. Then inside it, for each item you want to add to the list, you have to include it inside the \<li> tag, which stands for List Item.
It is indented by default. You can also add the "type" attribute, with which you can determine the numbering system you want; you have roman numerals, numbers, letters, and more. You would better change the type by CSS.

```html

<ol type ="roman">
    <li>The first item</li>
    <li>The seecond item</li>
</ol>

```

### Unordered lists

You might use this kind of list when you want to make a list without any specific order for the items. You create it using \<ul> tag, and inside it, each item should be enclosed in the \<li> tag as well.
It is indented by default and has a type attribute with which you can determine the numbering type; you can have bullet point, diamond, square, and more. You would better change the type by CSS.

```html

<ul type ="diamond">
    <li>The first item</li>
    <li>The seecond item</li>
</ul>

```

### Definition lists

\<dl> is used when you want to make a series of terms and their definitions. Inside the definition list, you add each term in a special tag called the definition term \<dt>, then you add the definition in the definition tag \<dd>.

```html

<dl>
    <dt>Term 1</dt>
    <dd>the term 1 definition</dd>
    <dt>Term 2</dt>
    <dd>the term 2 definition</dd>
</dl>

```

### Nested lists

We can also add a list inside the list item, and by this, we can have a nested list. It will appear more indented than the parent list, and the browser will change the style of its numbering.


```html

<ul>
    <li>The first item</li>
    <li>the second item
        <ul>
            <li>The first child item for second</li>
            <li>The seecond child item for second</li>
        </ul>
    </li>
</ul>

```


## CSS Boxes

CSS deals with every element on the web page as a box. These boxes consist of three layers. The first layer is the content layer enclosed into a box with height, width, and padding. The padding is the space that separates the content from the next layer; the Border. Borders have width, color, and style. Besides, they can be modified to have rounded edges. The last layer is the margin that separates the whole element from its surrounding ones. We can specify a width for the margin to push the element away towards a certain direction.

### Box size

By default, the box's size fits the contents inside it, but most of the time, programmers want to change the box size according to the design requirements.
In general, we can specify box dimensions by two main properties; height and width. Dimension measures could be in pixels, rems, ems, and percentages. Pixel is the most commonly used unit by web programmers since it can provide the exact and accurate length for the height and width. However, it is an absolute unit, so it can not feature responsive design. Percentages and ems are good to give relative measures. The percentage is relative to the enclosing container, whether it is a div or the whole body box, while ems are relative to the font size of the box's content.

```css
/* this code was taken from duckett book */

div.box {
height: 300px;
width: 300px;
background-color: #bbbbaa;}
p {
height: 75%;
width: 75%;
background-color: #0088dd;}

```

### Limiting width and height

It is considered best practice to limit your elements' height and width when building a responsive web page design. Consequently, when you control the width limit, your page's content will not appear too wide on wide screens and not too narrow on small screens.
We might even want to limit the height of the content, so it will fit comfortably and conform to the rest of the page's contents.

```css
/* this code was taken from duckett book */
td.description {
min-width: 450px;
max-width: 650px;
}

p {
min-height: 10px;
max-height: 30px;}

```

### Overflow

For height limits, sometimes content will be relatively large when screens are minimized so that the content will flow over its container and overlap with other tight containers' contents. Fortunately, we can prevent this problem from occurring by determining the max height.
There are two values for the overflow property; hidden, which hide the overflowing content inside the box, and scroll, which gives the user a scroll bar to continue reading or showing the rest of the content by scrolling up and down.

```css
/* this code was taken from duckett book */
p.one {
overflow: hidden;}
p.two {
overflow: scroll;}

```
