```html
<style>
  /* a comment */
  .classname {
	color: red;
  }
</style>
```

`.classname` is the selector. It's used to select elements in the HTML

## Class
Preceding with a `.` dot will make it match a `class` so it can be applied to specific elements

```html
<span class="classname">Some blue text</span>
```

## ID
Preceding with a `#` hash will make it match an `id` so it can be applied to one specific element. There should only be one instance of any particular `id` on a page.

```html
<style>
  #my-special-heading {
	color: red;
  }
</style>

<div id="my-special-heading">
  <h1> Nice </h1>
</div>
```

## Universal selector
Using a `*` (universal selector) will apply the style to everything

```html
<style>
  * {
    color: blue;
  }
</style>

<p>
  Hey everything's blue now....... as it should be
</p>
```

## Tag name
Using the name of a tag will style all instances of that tag
```html
<style>
  a {
    color: purple;
  }
</style>

<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ" title="Click it, I dare you">You've definitely clicked this before, see the link is purple!</a>
```

## Combinators
You can combine the above selectors.

Consider the following HTML

```html
<!-- Yoinked straight from the lecture slides -->
<div class="A">
  <span class="B">one</span>
  <span class="C">two</span>
  <span class="B">three</span>
  <span class="B">four</span>
  <div>
    <span class="B">five</span>
  </div>
</div>
<span class="B">six</span>
```

**Decendant**: all `.B` elements inside `.A`
Selects one, three, four, five
```css
.A .B { color: red; }
```

**Child**: all `.B` which are direct children of `.A`
Selects one, three, four
Note that five is not selected as it is a grandchild of `.A`
```css
.A > .B { color: blue; }
```

**Adjacent sibling**: any `.B` that directly follows a `.C`
Selects three
```css
.C + .B { color: purple; }
```

**General sibling**: any `.b` that follows a `.c`
Selects three, four
```css
.C ~ .B { color: green; }
```

## Pseudo-classes

`selector:pseudo-class` selects elements with a special state

Selects a button that has the user's mouse hovering over it
```css
button:hover { background-color: white; }
```

Selects an input that has the user's cursor focused on it
```css
input:focus { color: pink; }
```

Selects an [[anchor]] that has been visited.
```css
a:visited { color: pink; 
/* Yep, you definitely clicked on that rickroll, didn't you */
```
