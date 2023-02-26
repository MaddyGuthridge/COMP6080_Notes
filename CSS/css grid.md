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
  grid-template-rows: 1fr 2
}
```