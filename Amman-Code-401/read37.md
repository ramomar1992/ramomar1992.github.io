# Redux - Combined Reducers

When the application grows bigger, the number of states that we want to maintain the user experience and the whole workflow of the application also increases. Therefore, we tend to create multiple reducers for each state instead of making one giant reducer that holds all the information and the functions we want to execute.

Redux solved this problem by introducing the `.combineReducer({reducer_1,reducer_2,...})` function. This function takes multiple reducers as an object argument and return one single reducer that manages all the dispatch actions from it. What happens when we dispatch an action is that combineReducer invokes all the reducers at once giving each reducer a chance to respond to the action being dispatched. This behavior is somehow not so efficient but it gets the job done, and it will retain the consistency of the whole application work flow.

We can avoid using combineReducers and build our own reducer instead, or, also, we can keep using reducers individually without combining them. This also works. However, The drawbacks and bugs are with a higher chance to occur and there is no reason to not use `.combineReducers()` under any circumstance. 

## Rules we should follow when using `combineReducers`

1. For any action that is not recognized, it must return the state given to it as the first argument.
2. It must never return undefined. It is too easy to do this by mistake via an early return statement, so combineReducers throws if you do that instead of letting the error manifest itself somewhere else.
3. If the state given to it is undefined, it must return the initial state for this specific reducer. According to the previous rule, the initial state must not be undefined either. It is handy to specify it with ES6 optional arguments syntax, but you can also explicitly check the first argument for being undefined.

While combineReducers attempts to check that your reducers conform to some of these rules, you should remember them, and do your best to follow them. combineReducers will check your reducers by passing undefined to them; this is done even if you specify initial state to Redux.createStore(combineReducers(...), initialState). Therefore, you must ensure your reducers work properly when receiving undefined as state, even if you never intend for them to actually receive undefined in your own code.
