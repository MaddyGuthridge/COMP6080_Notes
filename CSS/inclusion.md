There are a variety of ways to include [[CSS]] in a document

## Import from external file
```html
<!-- Link to external CSS stylesheet -->
<link rel="stylesheet" href="style.css" />
```

```css
/* style.css */
.classname {
  color: red;
}
```

- Browser can cache, speeding up load-times
- Use [[selectors]] in [[CSS]] to select elements of the [[HTML]]
- **Preferred method**

## Inline
```html
<!-- CSS using the style property -->
<div style="color: red">some text</div>
```

- Good for quick hacking around, since you won't mess with other stuff

## In document
```html
<style>
  /* CSS in a style tag */
  .classname {
	  color: red;
  }
</style>
```

- Not used that much except for experimentation
- Use [[selectors]] in [[CSS]] to select elements of the [[HTML]]
