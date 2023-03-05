Used to get user input.
```html
<form>
  <input type="text" name="login">
</form>
```

Access in JS using `document.forms`
```js
document.forms.test // form with name "test"
document.forms[0] // first form in document
```

Elements can be accessed using
```js
let form = document.forms.someForm;
let ele = form.elements.someElement;
// or
ele = form.someElement;
```

## Inner tags

- [[input]] - used for most inputs, but apparently not all of them because there is no such thing as consistency
- [[select]] - used for drop-down boxes