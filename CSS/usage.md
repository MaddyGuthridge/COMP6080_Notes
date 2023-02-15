```html
<style>
  /* a comment */
  .classname {
	color: red;
  }
</style>
```

`.classname` is the selector. It's used to select elements in the HTML

Preceding with a `.` dot will make it match a `class` so it can be applied to specific elements

```html
<span class="classname">Some blue text</span>
```

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

Using the name of a tag will style all instances of that tag
```html
<style>
  a {
    color: purple;
  }
</style>

<a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ">You've de
```