# Review, Research, and Discussion

## Array.map()

It is an array prototype performed on arrays and returns a new array with the same length as the starter array. We can perform any operations on the elements of the starter array, and the returned value will be assigned to the corresponding position of the new array. It takes a callback function with two main default arguments that should be manually supplied; index and current element. If the started array contains all nulls, the returned array will also return nulled values.

## Array.reduce()

It is also an array prototype that is performed on arrays of any type. It takes a callback, and a start value assigned to a default argument called the accumulator. The returned value will be assigned to the accumulator and processed again with the callback function until all elements are exhausted. The final accumulated value will be returned, and the method will terminate. The callback function takes three main default arguments; accumulator, index, and element.

## superagent()

```node

function getResultFromApi(req,res){

const url='API to fitch';

superagent.get(url).then(result=>{

return result.body).then(result=>{ res.render('index',{sendRes:result})

});

}

```

## Promises Functions(Asynchronous)

A promise is commonly defined as a proxy for a value that will eventually become available.Promises are one way to deal with asynchronous code, without getting stuck in callback hell. Promises have been part of the language for years (standardized and introduced in ES2015), and have recently become more integrated, with async and await in ES2017. Async functions use promises behind the scenes, so understanding how promises work is fundamental to understanding how async and await work.

- How promises work, in brief

Once a promise has been called, it will start in a pending state. This means that the calling function continues executing, while the promise is pending until it resolves, giving the calling function whatever data was being requested. The created promise will eventually end in a resolved state, or in a rejected state, calling the respective callback functions (passed to then and catch) upon finishing
