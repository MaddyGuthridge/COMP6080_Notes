Callback functions are functions that are called when some operation completes. They are triggered through the [[event loop]].

```js
// Wait 2 seconds
// We give a callback which is called once the timeout expires
setTimeout(() => {
  console.log("We waited")
}, 2000);
```