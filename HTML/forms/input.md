There are many types of input elements used in [[form]]s.

## `text`
Text box
```js
let textContents = input.value;
```

## `password`
Text box for passwords, contents are hidden.

## `checkbox`
You can tick multiple of them
```js
let chosen = input.checked;
```

## `radio`
You can select one of them
```js
let chosen = input.checked;
```

## `submit`
A button that submits the form.
Listen for the submit event using
```js
form.addEventListener('submit', (event) => {
  event.preventDefault();
  // Do form validation and the like
})
```