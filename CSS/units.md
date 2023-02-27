## `px`
Pixels (CSS pixels, not physical pixels on the device, provided you've used the right [[meta]] tags)

## `em`
Width of a capital M - used for font sizes. (see [[text properties]])

## `rem`
Relative width of a capital M - this one doesn't stack when used in a nested fashion - use it instead of `em` where possible.

## percent `%`
As a percentage of the default, or a percentage of the available space.

- `100%` means standard font size for text
- `50%` means taking up half the available space for [[div]] elements and the like

## `vw`
A percentage of the [[viewport]] width. 

Note that if the scroll bar takes up space (like it does in bad operating systems such as Windows), that will contribute to the width and your content will overflow.

## `vh`
A percentage of the [[viewport]] height.

Note that if the address bar auto-hides, it will contribute to the width, so your content will just overflow. To make something fit the whole screen, you should just give up, it's too difficult