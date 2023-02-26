Powerful tool for having things automagically resize and regroup.

See: [CSS Tricks: A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

Compare with: [[css grid]]

Use properties
```css
.container {
	display: flex;
	flex-direction: row-reverse;
	justify-content: flex-end;
	align-items: center;
}
```

### `flex-direction`

Order to put elements

### `justify-content`

How to space things out:

- `flex-start` - align left
- `flex-end` - align right
- `center` - align center
- `space-between` - equal space between elements
- `space-around` - equal space around elements
- `space-evently` - make everything equally spaced, accounting for content size

### `align-items`

How to align items vertically within the container

### `flex-wrap`

What to do when things overflow.

- `wrap`: wrap content

## Properties of elements

### `flex`

Ratio to use when distributing content. Defaults to `1`, but setting to `2` would make the item width twice that of the other items.