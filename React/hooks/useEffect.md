Used to trigger changes in a [[component]] whenever some kind of event happens.

```jsx
useEffect(() => {
	// Code to set up effect
	// Adding an event listener and the like

	return () => {
		// Code to clean up effect
		// Removing that event listener and the like
	}
}, [ /* dependencies */ ]);
```

## Setup
`useEffect` is given a [[callback]] function, which is called just after the component has rendered. It should set up the effect (eg starting a timer, adding an event listener, or fetching data).

It then should return a cleanup function.

## Cleanup
The setup function needs to return a cleanup function, which undoes any changes caused by the setup. This is important as otherwise we may leave random JS floating around breaking things in future.

## Dependencies
An optional list of reactive values that the effect needs to interact with.

Dependencies can be:
- [[useState]]
- [[props]]
- Any functions inside your component body

### If provided
Any change to the given dependencies will cause the effect to be rerun.

### If empty
The effect is run once when the component is rendered for the first time.

### If omitted
The effect is run on every re-render of the component.
