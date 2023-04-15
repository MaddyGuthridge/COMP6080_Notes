Testing framework for [[JavaScript]].

## Syntax
```js
// Callback to create the test
test('name of the test', () => {
	// Make sure the value on the left equals the value on the right
	expect(2 * 5 * 6 * 7).toStrictEqual(420);
})
```
