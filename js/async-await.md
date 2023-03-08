Basically a cleaner way to use [[promises]].

First declare an `async` function. Turns your entire function into a promise
```js
const doThing = async () => {
  // stuff
}
```

Then use `await` to resolve promises synchronously and cleanly.
```js
const doThing = async () => {
  // We wait for the promise to resolve
  let result = await somePromiseFunction();
}
```

## Pros
- Much more readable
- Much more usable

## Cons
- Still need to understand promises
- Is blocking, so not good for concurrency