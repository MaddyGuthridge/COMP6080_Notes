Essentially a much more stylable table element.

## What to use
- Table when representing a literal table
- CSS Grid when representing anything else in a table

## Units
`fr` (means *fraction* of grid)

## Sizes
Specify sizes of rows/cols as follows

```css
#container {
  display: grid;
  /* 3 columns of equal spacing */
  grid-template-columns: 1fr 1fr 1fr;
  /* 2 rows with the bottom row being twice as tall as the top row */
  grid-template-rows: 1fr 2fr;
}
```

You can then fill content like this:

```html
<body>
  <div id="container">
    <!-- first row -->
    <div>Some content</div>
    <div>Some content</div>
    <div>Some content</div>
    <!-- second row -->
    <div>Some content</div>
    <div>Some content</div>
    <div>Some content</div>
	</div>
</body>
```

## Areas

You can also specify areas as follows

```css
#container {
  display: grid;
  grid-template-columns: 1fr 8fr 1fr;
  grid-template-rows: 1fr 3fr 1fr;
  /* Label each area */
	grid-template-areas:
		"header header header"
		"sidebar main main"
		"footer footer footer";
}

/* Now create classes for each template */
.header {
  /* Items with this class will be placed in the right place automatically */
  grid-area: header;
}
.footer {
  grid-area: footer;
}
.sidebar {
  grid-area: sidebar;
}
.main {
  grid-area: main;
}
```

Content can be placed correctly using the classes.

```html
<body>
  <div id="container">
    <!-- Content gets placed in the correct spot -->
    <div class="header">My header</div>
    <div class="footer">My footer</div>
    <div class="main">My body</div>
    <div class="sidebar">My sidebar</div>
	</div>
</body>
```

## Spacing

Use `row-gap` and `column-gap` properties. For overall use the `gap` property.