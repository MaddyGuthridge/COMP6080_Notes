ARIA (Accessible Rich Internet Applications) is a collection of additional attributes to supplement [[HTML]]. 

Should be used "sparingly and thoughtfully" on top of existing HTML tags and roles.

## Add labels for icon-only buttons
```html
<button aria-label="Show menu" />
```

## Add state for custom elements

```html
<!-- indicate that the element is a toggle -->
<button
	role="switch"
	aria-checked={true}
/>
```

## Specify that a pop-up is model
```html
<!-- 
	Indicate that a pop-up is a modal, and that normal behaviour will resume
	on dismissal.
-->
<div
	role="alertdialog"
	aria-modal={true}
>
  Sign in to perform this action
</div>
```

## Specify relationships between elements
```html
<button
	aria-controls="menuElem"
	aria-expanded={true}
	aria-haspopup="menu"
>
	Show menu
</button>
<aside id="menuElem"> ... </aside>
```

- `aria-controls` - associate ID of similar elements
- `aria-expanded` - whether content is expanded or not
- `aria-haspopup` - tell ARIA about the type of popup
	- `menu`
	- `listbox`
	- `dialog`