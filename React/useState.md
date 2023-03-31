`useState` is a function in [[React]] used to tell it when it needs to rerender a component.

The function returns an array containing the value, and a function to set the value.

```jsx
// Use array unpacking to get the functions cleanly
const [myValue, setMyValue] = useState(42);
```