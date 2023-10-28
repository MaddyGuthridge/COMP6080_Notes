In [[JavaScript]], data can be stored on the user's machine with local storage.

It is most often used for keeping track of user settings and the like.

## Cons

- NOT SECURE!!! Don't use it for sensitive info.
- Might hit quota limit if other websites are using lots of data (yes that's right you can waste the storage space of other websites)
- Only stores strings, so need to use JSON serialisation for it or something

Access using
```javascript
let value = localStorage.getItem('key')
localStorage.setItem('key', value)
```

## Alternatives
For bigger projects, consider [[Redux]].