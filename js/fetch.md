Basically [[xhr|XHR]] except good.

```js
const url = 'https://api.chucknorris.io/jokes/random';

// GET request by default
// Can also supply a { method: 'POST' } to specify request type
fetch(url)
	.then(res => {
		// Status code 200
		if (res.ok) {
			// Get the JSON
			// This gives a promise which we can handle below
			return res.json();
		} else {
			// Reject the promise so it can be caught below
			throw new Error(`${res.status}`);
		}
	})
	.then(json => {
		// We received the parsed JSON from the .then above,
		// and can now handle it
		console.log(json);
	})
	.catch(e => {
		console.error(`Error: ${e}`)
	});
```

## Limitations
- XHR works on very old browsers, fetch does not
- XHR gives download progress - to do it in a modern way, use the streams API
- XHR can be easily cancelled
