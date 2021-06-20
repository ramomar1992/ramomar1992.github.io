# Hooks API

What is a Hook? A Hook is a special function that lets you “hook into” React features. For example, useState is a Hook that lets you add React state to function components. We’ll learn other Hooks later. If you write a function component and realize you need to add some state to it, previously you had to convert it to a class. Now you can use a Hook inside the existing function component. We’re going to do that right now!

Hooks are new addition to the React API. They allow us to transform component functions to be stateful and share stateful logic among components. It adds new features to component functions that were not there in previous ones. It adds states to the components, they allow components to use lifecycle events and methods without being inside a class, and many more new features.

## State Hooks

In a function component, we have no this, so we can’t assign or read this.state. Instead, we call the useState Hook directly inside our component. We can require the useState function from the react package, then we can use it to destructor two special elements from it. The first element is the state variable and we can call it anything we want. The other element is a function that is used to reset the state variable, and we can call it anything we want as well.

This is a way to “preserve” some values between the function calls — useState is a new way to use the exact same capabilities that this.state provides in a class. Normally, variables “disappear” when the function exits but state variables are preserved by React.

### What do we pass to useState as an argument?

The only argument to the useState() Hook is the initial state. Unlike with classes, the state doesn’t have to be an object. We can keep a number or a string if that’s all we need. In our example, we just want a number for how many times the user clicked, so pass 0 as initial state for our variable. (If we wanted to store two different values in state, we would call useState() twice).

### Using Multiple State Variables

Declaring state variables as a pair of [something, setSomething] is also handy because it lets us give different names to different state variables if we want to use more than one. You don’t have to use many state variables. State variables can hold objects and arrays just fine, so you can still group related data together. However, unlike this.setState in a class, updating a state variable always replaces it instead of merging it.

## Effect Hooks

The Effect Hook lets you perform side effects in function components.

### Effects Without Cleanup

Sometimes, we want to run some additional code after React has updated the DOM. Network requests, manual DOM mutations, and logging are common examples of effects that don’t require a cleanup.

We use the effect methods by importing useEffect element from the react package. We then use it directly inside the component function. It takes a callback that performs the effect logic.

#### What does useEffect do?

By using this Hook, you tell React that your component needs to do something after render. React will remember the function you passed, and call it later after performing the DOM updates. In this effect, we set the document title, but we could also perform data fetching or call some other imperative API.

#### Why is useEffect called inside a component?

Placing useEffect inside the component lets us access the count state variable (or any props) right from the effect. We don’t need a special API to read it — it’s already in the function scope. Hooks embrace JavaScript closures and avoid introducing React-specific APIs where JavaScript already provides a solution.

#### Does useEffect run after every render?

Yes! By default, it runs both after the first render and after every update. Instead of thinking in terms of “mounting” and “updating”, you might find it easier to think that effects happen “after render”. React guarantees the DOM has been updated by the time it runs the effects.

Unlike componentDidMount or componentDidUpdate, effects scheduled with useEffect don’t block the browser from updating the screen. This makes your app feel more responsive. The majority of effects don’t need to happen synchronously. In the uncommon cases where they do (such as measuring the layout), there is a separate useLayoutEffect Hook with an API identical to useEffect.

### Effects with Cleanup

You might be thinking that we’d need a separate effect to perform the cleanup. But code for adding and removing a subscription is so tightly related that useEffect is designed to keep it together. If your effect returns a function, React will run it when it is time to clean up.

#### Why did we return a function from our effect?

This is the optional cleanup mechanism for effects. Every effect may return a function that cleans up after it. This lets us keep the logic for adding and removing subscriptions close to each other. They’re part of the same effect!

#### When exactly does React clean up an effect?

React performs the cleanup when the component umount. However, as we learned earlier, effects run for every render and not just once. This is why React also cleans up effects from the previous render before running the effects next time.

## Rules of Hooks

### Only Call Hooks at the Top Level

Don’t call Hooks inside loops, conditions, or nested functions. Instead, always use Hooks at the top level of your React function, before any early returns. By following this rule, you ensure that Hooks are called in the same order each time a component renders. That’s what allows React to correctly preserve the state of Hooks between multiple useState and useEffect calls.

### Only Call Hooks from React Functions

Don’t call Hooks from regular JavaScript functions. Instead, you can:

* Call Hooks from React function components.
* Call Hooks from custom Hooks

### how does React know which state corresponds to which useState call?

React relies on the order in which Hooks are called. As long as the order of the Hook calls is the same between renders, React can associate some local state with each of them. This is why Hooks must be called on the top level of our components. If we want to run an effect conditionally, we can put that condition inside our Hook.
