XML HTTP Request

A way to fetch data from a backend. It's old and clunky (it doesn't even use [[promises]], ew), so use [[fetch]] instead.

It can be used with JSON and other data types, not just XML (thankfully). The name is just archaic.

```js
const url = 'https://api.chucknorris.io/jokes/random';
const xhr = new XMLHttpRequest();

// We're performing a GET request
xhr.open("GET", url);

xhr.onload = () => {
	// Check that the request succeeded
	if (xhr.status === 200) {
		const meme = JSON.parse(xhr.response);
		console.log(meme);
	} else {
		console.error(`Error with request: ${xhr.status}: ${xhr.response}`);
	}
}

xhr.onerror = () => {
	console.error("Error sending request");
}
```