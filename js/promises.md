Rather than getting yourself into "callback hell", you can use promises to chain asynchronous code together.

In essence, a function can return a promise, which you can then wait for as follows:

```js
const ipromise = loadSomething();

// Do any other things we need to do

// Once it's done, we can wait for the promise to resolve
ipromise
  .then(data => {
    // Called if the promise resolves successfully
    console.log("Got the data!", data);
})
  .catch(err => {
    // Called if the promise is rejected (ie an error happened)
    console.log("Got an error!", err);
});
// Note that it we `.then` on multiple promises they could happen in any
// order
```

## Creating promises

```js
function makeAPromise(arg) {
  // This function runs asynchronously and can
  // resolve or reject the promise
  function promiseHandler(resolve, reject) {
    if (arg === 42) {
      // Resolve it by calling the resolve function
      resolve("Ah, the answer!");
    } else {
      // Or reject it with the reject function
      reject("Alas, it is not the answer");
    }
  }
  // We just need to create our promise using the Promise constructor
  return new Promise(promiseHandler);
}
```

## Chaining promises

```js
// We wait for the result of the first
first_promise.then(data => {
  console.log("First");
  // And it gets us to wait for the result of the second
  return second_promise;
}).then(data => {
  console.log("Second");
})
```

## Other neat things with promises

```js
// A promise that resolves if all the given promises have resolved
// If any promises reject, then it will reject
Promise.all([...promises]);
// A promise that resolves when all the promises have settled, 
// regardless of whether they were successful
Promise.allSettled([...promises]);
// A promise that resolves if at least one promise resolves successfully,
// but which still waits for all the promises to settle
Promise.any([...promises]);
// Like Promise.any, but it resolves as soon as one of the promises given
// resolve
Promise.race([...promises]);
```