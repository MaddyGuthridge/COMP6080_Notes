`useState` is a function in [[React]] used to tell it when it needs to rerender a component.

The function returns an array of the data, and a function to set the data.


```jsx
// Use array unpacking to get the functions cleanly
let [myValue, setMyValue] = useState(42);
```