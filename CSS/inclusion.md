## Import from external file
```html
<link rel="stylesheet" href="style.css" />
```

- Browser can cache, speeding up load-times
- Preferred

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

## What to use
- Prefer external file
- Only use inline when hacking/testing