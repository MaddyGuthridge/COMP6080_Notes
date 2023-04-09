Before functional [[component|components]], there was class components.

Basically, instead of declaring a component as a function, you'd declare it as a class.

```jsx
class App extends React.Component {
	// Create
  constructor(props) {
    super(props);
    this.state = {
	    name: '',
	    age: 0,
    };
  }

	componentDidUpdate(prevProps, prevState) {
		// Called when the component is updated
	}

	render() {
		// Render the component
		return (
			<div>
				<p>Hello, {this.state.name}! You are {this.state.age} years old.</p>
			</div>
		)
	}
}
```

## Changing the state
```js
// Yuck, so verbose
this.setState({ ...this.state, any, new, values });
```
