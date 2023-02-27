Allows you to do "if statement" logic to selectively apply styles when conditions are met.

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
