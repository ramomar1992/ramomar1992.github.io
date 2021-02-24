# CSS Transforms, Transitions, and Animations

## Transform

Transform is a fabulous tool to manipulate the positioning and size of an element. It is a new feature that expands our ability to make them appear like 3d shapes, whether we play them in 2d or 3d.

There are several transform properties we can change:

### Rotate

This property allows us to rotate elements on any axes, and it takes degree values.

```css

div{
  transform: rotate(20deg);
}

```

### Scale

Using the scale allows us to change the size of the element and how it looks. It takes values from 0 - 1 to make the element appear smaller, while to make it larger, we can give it a number more than 1. We can also scale the element on a specific axis, so if we want to scale it on the x-axis, we can type scaleX or scaleY for the y axis.

```css

.box-1 {
  transform: scale(.75);
}
.box-2 {
  transform: scale(1.25);
}


```

### Translate

This property makes it easy to reposition the element on the different axes, just like the relative positioning. We can type, translate and supply two values; the first should be for the x and the second for the y axis. We can also set them individually with transformX and transformY.

```css

div {
  transform: translateY(25%);
}
div {
  transform: translate(-10px, 25%);
}


```

### Skew

The skew property lets us skew the element on the respective axis, and it makes elements appear steeper from different angles. It takes degree values. This property does not work for 3d transformation.

```css

div {
  transform: skewY(-20deg);
}
div {
  transform: skew(5deg, -20deg);
}


```

### Combining transform

We can combine multiple transforms, but we do not separate them with commas.

```css

div {
  transform: skew(10deg, 20deg) translateX(20px);
}


```

### Transform origin

Without changing the origin of the transform, the origin will be the element axis's middle point, 50% on the horizontal axis and 50% on the vertical axis. We can change the origin by transform-origin property. We can use it on one axis or both axes.  

```css

div {
  transform: scale(.5);
  transform-origin: 100% 100%;
}
div{
  transform: skewX(20deg);
  transform-origin: top left;
}
div{
  transform: scale(.75) translate(-10px, -10px);
  transform-origin: 20px 50px;
}


```

There are also many more properties that work for transform:

* perspective
* perspective-origin
* transform-style
* backface-visibility

## Transitions

With CSS3 transition property, we can make elements interactive when their state is changed, such as when it is hovered over, active, target, and focused on. The best way to trigger the state to transition is with the use of pseudo-classes. There are four transition properties related to any HTML element: transition-property, transition-duration, transition-timing-function, and transition-delay.

### Transiion property

This property determines exactly which property the transition is targeting. So if we choose one property, it alone will be affected; other properties will not. So, it is possible to supply more than one property separated with a comma to this part. If you want to apply the transition to all properties, you can type all instead.

```css

div{
    transition-property: border-radius;
}

```

Note: not all properties can be transitioned, only properties with a liable midpoint value during the transition. We can apply the transition to offset and colors, but we can't use it with the display.

### Transition duration

This property sets the duration of time in which the transition should occur. It is specified with general time measurements like seconds or milliseconds. We can determine multiple duration for different properties selected by separating each duration with a comma from the other.

```css
div{
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
}

```

### Transition timing

This property can take several values, each of which determines the speed and the pace at which the transition will be moving. For example, ease-in starts slow, then it becomes faster, ease-out is the opposite to ease-n, and many more. We can select as many timing as there are properties, but we have to separate them with commas.

```css

div{
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear, ease-in;
}


```

### Transition delay

Using this part of the transition, we can determine how long the transition should wait before it starts.

```css
div{
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear, ease-in;
  transition-delay: 0s, 1s;
}

```

### Shorthand transitioned

We can replace all these four properties with the only one, which is a shorthand, but we have to be careful with the order of how we write the properties inside it. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly, transition-delay. Do not use commas with these values unless you are identifying numerous transitions.

```css

div{
      transition: background .2s linear, border-radius 1s ease-in 1s;
}

```

## Animations

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple transition points upon different keyframes.

Transition is very good in most situations, but when we need more control over the element's movement, we need to use animation since it opens the power gates to innovate and be creative.

Animation allows us to set multiple breakpoints; when the timing hits these breakpoints, the movement will change depending on the properties we intend to change in their state. We wrap all these breakpoints into a keyframes identifier.

The keyframes identifier takes a name and multiple breakpoint values represented by percentages; for 0%, we can type from instead, and for 100%, we can type to.

```css

@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}


```

### Animation name

This property takes the name specified to the keyframes rules. It is applied to the element we want to animate.

```css

.stage:hover .ball {
  animation-name: slide;
}


```

### Animation duration, Time function, and delay

After we give the animation name, we have also to specify the duration for which it will animate, and we can give a time function just like we did with transition and a delay.

```css

.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
}

```

### Animation iteration

When we run the animation, it will run only once. If we want it to repeat more times, we can add the animation-iteration-count. It takes integer or infinite. The integer will make it run as many times the integer's value, and the infinite will keep it run forever.

```css

div{
animation-iteration-count: infinite;
}

```

There are also many more properties:

* animation-direction
* animation-play-state
* animation-fill-mode

```css

.ball{
  animation-fill-mode: forwards;
  animation-direction: alternate;
}

.stage:active .ball {
  animation-play-state: paused;
}


```

### Shorthand Animations

Fortunately, animations, just like transitions, can be written out in a shorthand format. This is accomplished with one animation property rather than multiple declarations. The order of values within the animation property should be animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count, animation-direction, animation-fill-mode, and lastly, animation-play-state.

```css

.stage:hover .ball {
  animation: slide 2s ease-in-out .5s infinite alternate;
}
.stage:active .ball {
  animation-play-state: paused;
}

```
