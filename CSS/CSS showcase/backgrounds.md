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
	  white 100%
  );
}
```

### `radial-gradient()`
Create a gradient from a point.
