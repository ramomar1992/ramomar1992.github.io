# Application State with Redux

* Redux is a predictable state container for JavaScript apps.
* The createStore factory function from Redux is used to create a Redux STORE.
* The Reducer is the only mandatory argument passed into createStore()
* A REDUCER is just a function. A function that takes in two parameters. The first is the STATE of the app, and the other is an ACTION.
* A Reducer always returns the new state of your application.
* The Initial State of your application, initialState is the second argument passed into the createStore function call.
* Store.getState() will return the current state of your application. Where Store is a valid Redux STORE.

## What it does?

Redux takes away some of the hassles faced with state management in large applications. It provides you with a great developer experience, and makes sure that the testability of your app isn’t sacrificed for any of those.

## why to use Redux?

1. In larger apps with a lot of moving pieces, state management becomes a huge concern. Redux ticks that off quite well without performance concerns or trading off testability.

2. The developer experience that comes with it. Include logging, hot reloading, time travel, universal apps, record and replay

## State Updates with Actions

* Unlike setState() in pure React, the only way you update the state of a Redux application is by dispatching an action.
* An action is accurately described with a plain JavaScript object, but it must have a type field.
* In a Redux app, every action flows through the reducer. All of them.
* By using a switch statement, you can handle different action types within your Reducer.
* Action Creators are simply functions that return action objects.
* It is a common practice to have the major actors of a redux app live within their own folder/directory.
* You should not mutate the state received in your Reducer. Instead, you should always return a new copy of the state.
* To subscribe to store updates, use the store.subscribe() method.

## How it works

Unlike setState() in pure React, the only way you update the state of a Redux application is if you make your intent known to the REDUCER. By dispatching actions. There’s just one thing to be aware of. An action must have a type field. This field describes the intent of the action.

## What is the best way to build applications with Redux

* It is a good practice to always plan your application development process before jumping into the code.
* In your state object, avoid nested entities at all cost. Keep the state object normalized.
* Storing your state fields as objects does have some advantages. Be equally aware of the issues with using objects, mainly the lack of order.
* The lodash utility library comes very handy if you choose to use objects over arrays within your state object.
* No matter how little, always take some time to design the state object of your application.
* With Redux, you don’t always have to pass down props. You can access state values directly from the store.
* Always keep a neat folder structure in your Redux apps, like having all major Redux actors in their own folders. Apart from the neat overall code structure, this makes it easier for other people to collaborate on your project as they are likely conversant with the same folder structure.
* Reducer composition is really great especially as your app grows. This increases testability and reduces the tendency for hard-to-track errors.
* For reducer composition, make use of combineReducers from the redux library.
* The object passed into the combineReducers function is designed to resemble the state of your application, with each value gotten from the associated reducers.
* Always break larger components into smaller manageable bits. It’s a lot easier to build your way up that way.
