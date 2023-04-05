Data can be stored on the user's machine with local storage.

Can be used to store settings and the like.

## Cons

- NOT SECURE!!! Don't use it for sensitive info.
- Might hit quota limit if other websites are using lots of data (yes that's right you can waste the storage space of other websites)
- Only stores strings, so need to use JSON serialisation for it

Access using
```js
let value = localStorage.getItem('key')
localStorage.setItem('key', value)
```
