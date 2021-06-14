# Props and State

## We can change the state using setState() only

setState() is the only legitimate way to update state after the initial state setup

### The concept of reconciliation in react

The reconciliation process is the way React updates the DOM, by making changes to the component based on the change in state. When the request to setState() is triggered, React creates a new tree containing the reactive elements in the component (along with the updated state). This tree is used to figure out how the Search component’s UI should change in response to the state change by comparing it with the elements of the previous tree. React knows which changes to implement and will only update the parts of the DOM where necessary. This is why React is fast.

The reconciliation process does not necessarily change the entire tree, except in a situation where the root of the tree is changed.

## Passing function to setState()

If we want ro perform more than on change in one call we can pass a function to the setState() that takes the previous state as the first arguemnt. This callback function will take care of changing the state

## Access Previous State Using Updater

When building React applications, there are times when you’ll want to calculate state based the component’s previous state. You cannot always trust this.state to hold the correct state immediately after calling setState(), as it is always equal to the state rendered on the screen.

setState() should be treated asynchronously — in other words, do not always expect that the state has changed after calling setState().

## Summart

When working with setState(), these are the major things you should know:

1. Update to a component state should be done using setState()
2. You can pass an object or a function to setState()
3. Pass a function when you can to update state multiple times
4. Do not depend on this.state immediately after calling setState() and make use of the updater function instead.