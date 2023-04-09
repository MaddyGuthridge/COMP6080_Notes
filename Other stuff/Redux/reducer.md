In [[Redux]], a reducer is a function that takes the [[store]] and an [[action]] and returns the new state after that action.

Reducers should take the form:
```js
const reducer = (state, action) => newState;
```

## For example
```js
function appReducer(state, action) {
  switch (action.type) {
    case 'increment':
	    return {
		    // All other data from the state so we don't delete anything
		    ...state,
		    // Increment the count
		    count: state.count + action.payload,
	    };
	  default:
		  // If we don't recognise the action, do nothing
		  return state;
  }
}
```