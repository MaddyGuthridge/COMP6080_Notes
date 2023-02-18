These can be applied to most things I think, but they work best on [[div]]s.

### `background-color`
Use a [[color|colour]] as the background

### `background-image`
Apply a background image to the element
```css
.my-fancy-div {
	background-image: url("https://i.ytimg.com/vi_webp/dQw4w9WgXcQ/maxresdefault.webp");
	background-size: 100% auto;
}
```
We need to specify the `background-size` or it might be too big.

This can also be done using various elements in the `background` property.

### `visibility`

Changes the visibility of elements
- `hidden`: space for element is taken, but no content is rendered
- `none`: no space for element is taken, useful for JavaScript