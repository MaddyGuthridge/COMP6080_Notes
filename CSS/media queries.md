Allows you to do "if statement" logic to selectively apply styles when conditions are met.

Often used to ensure that sites work well for both [[Mobile and Desktop]].

```css
@media (min-width: 600px) {
  .article: {
	  padding 10px 20px;
	}
}
```

If you define a `.article` property earlier, it will be overridden iff the media query gives true.

## Media types

Queries based on the kind of media

All device types:
```css
@media all { ... }
```

Page print-outs
```css
@media print { ... }
```

Screen devices
```css
@media screen { ... }
```

Screen readers
```css
@media speech { ... }
```

## Media features

Queries based on features and attributes of the device

Screen width - 500px and narrower probably indicates a phone
```css
@media (max-width: 500px) { ... }
```

Primary input can hover (eg mouse/trackpad)
```css
@media (hover: hover) { ... }
```

Prefers dark mode
```css
@media (prefers-color-scheme: dark) { ... }
```

## Combinations

You can combine conditions using logical operators.

Note that `not` inverts the entire query, not just the following expression.
```css
@media not screen
  and (min-width: 320px)
  and (orientation: portrait) {
    ...
  }
```

You can use commas like `or`

Applies to screen and print views
```css
@media screen, print {
  ...
}
```