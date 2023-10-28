In [[Redux]], an action is a [[JavaScript|JS]] object that describes an event or change that should happen to the [[store]].

## For example
```js
{
  // Type of action being taken, in this case, increment the count by 10
  type: 'increment',
  // Other info to go with the action
  payload: 10,
}
```

Obviously you could include other data - it is just a JS object after all. But you should always include a type property so that the reducers can distinguish between events.
