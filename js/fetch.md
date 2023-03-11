Basically [[xhr|XHR]] except good.

```js
const url = 'https://api.chucknorris.io/jokes/random';

// GET request by default
// Can also supply a { method: 'POST' } to specify request type
fetch(url)
	.then(res => {
		// Status code 200
		if (res.ok) {
			const meme = JSON.parse(res.);
			console.log(meme);
		}
	});
```