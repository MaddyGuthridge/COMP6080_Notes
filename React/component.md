In [[React]], you should build a page by creating a set of components, which can then be rendered.

Essentially, you create a function which returns [[JSX]] HTML, which gets rendered into a component.

```jsx
function MyButton() {
	return (
		<button>Oh wow, a button!</button>
	);
}

function App() {
	return (
		<>
			Hello world!
			// Embed the button into our app component
			<MyButton />
		</>
	)
}
```

## Customising React components
React components can be customised using [[props]].