[[head|Head]] tag to contain metadata about a page

```html
<meta name="Description" content="An awesome description of my site">
<meta name="Keywords" content="Comma, Separatated, Keywords">
<meta property="og:image" content="https://url.of/my/embeddable/image.png">
<meta property="og:image:type" content="image/png">
<meta property="og:image:width" content="436">
<meta property="og:image:height" content="228">
```

## Rendering tags

Tags used to ensure that things render correctly between [[mobile and desktop]].

These aren't the default because something something backwards compatibility.

Make the browser report the correctly scaled size of the page rather than the number of pixels the device has (which leads to tiny pages on phones)
```html
<meta 
	name="viewport"
	content="width=device-width"
>
```

Control the zoom of the page
```html
<meta
	name="viewport"
	content="initial-scale=1, maximum-scale=2"
>
```
