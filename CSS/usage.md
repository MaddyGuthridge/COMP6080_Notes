```html
<style>
  /* a comment */
  .classname {
	color: red;
  }
</style>

<span class="classname">Some blue text</span>
```

- `.classname` is the selector
- Preceding with a `.` dot will make it match a `class` so it can be applied to specific elements
- Preceding with a `#` hash will make it match an `id` so it can be applied to one specific element
	- There should only be one instance of any particular `id` on a page
- Using a `*` (universal selector) will apply the style to everything
- Using the name of a tag will style all instances of that tag