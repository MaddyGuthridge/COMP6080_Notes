`useState` is a [[React hook]] used to tell [[React]] when it needs to re-render a component, by notifying it when the state of something changes.

The function returns an array containing the value, and a function to set the value.

```jsx
// Use array unpacking to get the functions cleanly
const [myValue, setMyValue] = useState(42);
```

You can then bind the setter function to events to trigger a re-render.