To customise a [[React]] [[component]], make the component function accept a `props` object.

```jsx
function MyButton(props) {
	// Object destructuring
	const { myWidth, text } = props;
  return (
	  <button style={{ width: myWidth }}>{text}</button>
  );
}

function App() {
	return (
		<>
			<MyButton text="Button text" myWidth={100} />
		</>
	)
}
```

## Children
Any elements within an element will be passed to that element under the `children` prop.

```jsx
function MyButton(props) {
	const { children } = props;
	return (
		<button>{children}</button>
	);
}

function
```