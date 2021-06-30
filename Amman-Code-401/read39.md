# Redux - Tool-kit

The Redux Toolkit package is intended to be the standard way to write Redux logic. It was originally created to help address three common concerns about Redux:

* "Configuring a Redux store is too complicated"
* "I have to add a lot of packages to get Redux to do anything useful"
* "Redux requires too much boilerplate code"

Provide some tools that abstract over the setup process and handle the most common use cases, as well as include some useful utilities that will let the user simplify their application code.

Redux Toolkit also includes a powerful data fetching and caching capability "RTK Query". It's included in the package as a separate set of entry points. It's optional, but can eliminate the need to hand-write data fetching logic yourself.

## Redux Toolkit includes these APIs

* `configureStore()`: wraps createStore to provide simplified configuration options and good defaults. It can automatically combine your slice reducers, adds whatever Redux middleware you supply, includes redux-thunk by default, and enables use of the Redux DevTools Extension.
* `createReducer()`: that lets you supply a lookup table of action types to case reducer functions, rather than writing switch statements. In addition, it automatically uses the `immer` library to let you write simpler immutable updates with normal mutative code, like 'state.todo[3].completed = true'.
* `createAction()`: generates an action creator function for the given action type string. The function itself has toString() defined, so that it can be used in place of the type constant.
* `createSlice()`: accepts an object of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types.
* `createAsyncThunk()`: accepts an action type string and a function that returns a promise, and generates a thunk that dispatches pending/fulfilled/rejected action types based on that promise
* `createEntityAdapter()`: generates a set of reusable reducers and selectors to manage normalized data in the store
* `The createSelector()` utility from the Reselect library, re-exported for ease of use.

## Why to use Redux-Toolkit

1. Simple: Includes utilities to simplify common use cases like store setup, creating reducers, immutable update logic, and more.
2. Opinionated: Provides good defaults for store setup out of the box, and includes the most commonly used Redux addons built-in.
3. Powerful: Takes inspiration from libraries like Immer and Autobus to let you write "mutative" immutable update logic, and even create entire "slices" of state automatically.
4. Effective: Lets you focus on the core logic your app needs, so you can do more work with less code.

## How to use Redux-Toolkit

* Create a Redux store with `configureStore`
  * `configureStore` accepts a reducer function as a named argument
  * `configureStore` automatically sets up the store with good default settings
* Provide the Redux store to the React application components
  * Put a React-Redux `<Provider>` component around your `<App />`
  * Pass the Redux store as `<Provider store={store}>`
* Create a Redux "slice" reducer with `createSlice`
  * Call `createSlice` with a string name, an initial state, and named reducer functions
  * Reducer functions may "mutate" the state using `Immer`
  * Export the generated slice reducer and action creators
* Use the React-Redux `useSelector`/`useDispatch` hooks in React components
  * Read data from the store with the `useSelector` hook
  * Get the dispatch function with the `useDispatch` hook, and dispatch actions as needed
