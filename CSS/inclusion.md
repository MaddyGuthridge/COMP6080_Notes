There are a variety of ways to include CSS in a document

## Import from external file
```html
<link rel="stylesheet" href="style.css" />
```

- Browser can cache, speeding up load-times
- Use [[selectors]] in [[CSS]] to select elements of the [[HTML]]
- Preferred method

## Inline
```html
<div style="color: red">some text</div>
```

- Good for quick hacking around, since you won't mess with other stuff

## In document

```html
<style>
  .classname {
	color: red;
  }
</style>
```

- Good for quick work where multiple things need to use the same style
- Use [[selectors]] in CSS to select elements of the HTML
