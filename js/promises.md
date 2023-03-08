Rather than getting yourself into "callback hell", you can use promises to chain asynchronous code together.

In essence, a function can return a promise, which you can then wait for as follows:

```js
const iPromise = loadSomething();

// Do any other things we need to do

// Once it's done, we can wait for the promise to resolve
iPromise
  .then(data => {
    console.log("Got the data!", data);
})
  .catch(err => {
    console.log("Got an error!", err);
})
```