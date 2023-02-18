Fancy stuff you can do with backgrounds

### `linear-gradient()`
Create a gradient background

```css
/* A gradient */
.linear-1 {
	background: linear-gradient(
		to right,  /* can also be degrees, eg 123deg */
		green,
		pink
	);
}
```

```css
/* Using multiple points */
.linear-2 {
  background: linear-gradient(
	  to right,
	  purple 0%,
	  pink 20%,
	  red 40%,
	  orange 60%,
	  yellow 80%,
	  white 100%,
  );
}
```

### `radial-gradient()`
Create a gradient from a point. Usage similar to above.

### Repeating gradients
You can use a `repeating-` prefix to get a repeating variation of the above types. Space out the distances in `px` instead of `%`.
```css
.lines-1 {
	background: repeating-linear-gradient(
	  90deg,
	  blue 0px,
	  blue 10px,
	  purple 10px,  /* By placing this at the same point as earlier, we get 
	                   a solid line rather than a gradient at this point */
	  purple 20px
	  /* this pattern repeats forever */
	);
}
```

### Using multiple backgrounds
If you specify multiple backgrounds, they will be drawn one by one on top of each other.
