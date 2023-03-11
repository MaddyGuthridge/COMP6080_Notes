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
			// This gives a promise
			return res.json();
		} else {
			// Reject the promise so it can be caught below
			throw new Error(`${res.status}`);
		}
	})
	.then(json => {
		console.log(json);
	})
	.catch(e => {
		console.error(`Error: ${e}`)
	});
```