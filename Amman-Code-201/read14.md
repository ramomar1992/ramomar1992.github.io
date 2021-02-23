# CSS Transforms, Transitions, and Animations


## Transitions

With CSS3 transition property, we can make elements interactive when their state is changed, such as when it is hovered over, active, target, and focused on. The best way to triger the state to transition is with the use of pseudo-classes. There are four transition properties related to any HTML element which are transition-property, transition-duration, transition-timing-function, and transition-delay.

### Transiion property

This property deetermines exactly whic property the transition is targiting. So if we chosoe on property, it alone will be affected, other properties will not. So, it is possible to supply more than one property separated with comma to this part. If you want to apply the transition to all properties you can type all instead. 

```css

div{
    transition-property: border-radius;
}

```

Note: not all properties can be transitioned, only properties that have a liable midpoing value during the transition. For example, we can use transiion with offset and colors, but we can't use it with display.

### Transition duration

This property sets the duration of time in which the transition should occur. It is specified with general time measutemnt like seconds or miliseconds. We cam determine multible duration for different properties selected by separating each duration with comma from the other.

```css
div{
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
}

```

### Transition timing

This property can take several values, each of which determine the speed and the pace the transition will be moving according to. For example, ease-in starts slow then it becomes faster, ease-out is the opposite to ease-n, and many more. We can select as many timing as there are properties, but we have to separate them with commas.

```css

div{
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear, ease-in;
}


```

### Transition delay

Using this part of the transition, we can determine a period of time in which the transition should wait before it starts. 

```css
div{
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear, ease-in;
  transition-delay: 0s, 1s;
}

```

### Shorthand transitioned

We can replace all these four properties with only one which is a shorthand, but we have to be carefull with the oreder in which we wrtie the properties inside it. Using the transition value alone, you can set every transition value in the order of transition-property, transition-duration, transition-timing-function, and lastly transition-delay. Do not use commas with these values unless you are identifying numerous transitions.

```css

div{
      transition: background .2s linear, border-radius 1s ease-in 1s;
}

```

## Animations

Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

Transition are very good in most situations, but when we need more control over the movement of the element we need to use animation since it opens the power gates to innovate and to be creative. 

Animation allow us to set multiple breakpoints that when the timing hits these breakpoints the movement will change depending on the properties we intend to change their state. We wrape all these breakpoints into a keyframes identifier.

The keyframes identifier takes name and multiple breakpoint values represented by percetages, for 0% we can type from instead and for 100% we can type to.

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

This property takes the name specified to the keyframes rules. It is applyied to the element we want to animate.

```css

.stage:hover .ball {
  animation-name: slide;
}


```

### Animation duration, Time function, and delay

After we give the animation name, we have to also specify the duration for which it will animate and we can give a time function just like we did with transition and a delay as well. 

```css

.stage:hover .ball {
  animation-name: slide;
  animation-duration: 2s;
  animation-timing-function: ease-in-out;
  animation-delay: .5s;
}

```

### Animation iteration

When we run the animation it will run only once. If we want it to repeate more times, we can add the animation-iteration-count. It takes integer or infinate. The integer will make it run as many times the value of the integer, and the infinate will keep it run for ever.

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

Fortunately animations, just like transitions, can be written out in a shorthand format. This is accomplished with one animation property, rather than multiple declarations. The order of values within the animation property should be animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count, animation-direction, animation-fill-mode, and lastly animation-play-state.

```css

.stage:hover .ball {
  animation: slide 2s ease-in-out .5s infinite alternate;
}
.stage:active .ball {
  animation-play-state: paused;
}

```