Rather than getting yourself into "callback hell", you can use promises to chain asynchronous code together.

In essence, a function can return a promise, which you can then wait for as follows:

```js
const iPromise = loadSomething();

// Do any other things we need to do

// Once it's done, we can wait for the promise to resolve
iPromise
  .then(data => {
    // Called if the promise resolves successfully
    console.log("Got the data!", data);
})
  .catch(err => {
    // Called if the promise is broken (ie an error happened)
    console.log("Got an error!", err);
});
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