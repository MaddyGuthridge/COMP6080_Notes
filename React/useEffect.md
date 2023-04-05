Used to trigger changes in a component whenever some kind of event happens.

```jsx
useEffect(() => {
	// Code to set up effect
	// Adding an event listener and the like

	return () => {
		// Code to tear down effect
		// Removing that event listener, or something
	}
}, [ /* dependencies */ ]);
```

## Setup
`useEffect` is given a callback function, which is called just after the element has rendered. It should set up the effect (eg starting a timer, adding an event listener, or fetching data).

It then should return the tear-down function

## Tear-down
The setup function needs to return a tear-down function, which undoes any changes caused by the setup. This is important as otherwise we may leave random JS floating around breaking things in future.

## Dependencies
An optional list of triggers for the effect.

### If provided
