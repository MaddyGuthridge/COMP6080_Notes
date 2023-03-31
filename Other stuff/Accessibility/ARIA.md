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
	Indicate that a pop-up is a modal, and that normal behaviour will resume on dismissal 
-->
<div
	role="alertdialog"
	aria-modal={true}
>
  Sign in to perform this action
</div>
```