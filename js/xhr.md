XML HTTP Request

A way to fetch data from a backend. It's old and clunky (it doesn't even use [[promises]], ew), so use [[fetch]] instead.

It can be used with JSON and other data types, not just XML (thankfully). The name is just archaic.

```js
const url = 'https://api.chucknorris.io/jokes/random';
const xhr = new XMLHttpRequest();

// We're performing a GET request
xhr.open("GET", url);

xhr.onload = () => {
	if (xhr.status === 200) {
		const meme = JSON.parse(xhr.response);
		console.log(meme)
	}
}
```