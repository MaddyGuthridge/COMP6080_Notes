Not everyone uses a mouse/touchscreen. Make sure your web app supports other forms of input, such as the keyboard.

## Keyboard navigation
- Arrow keys and space to jump down the page
- Tab/shift+tab to navigate between interactive elements
- Etc etc

Don't set "keyboard traps" (where you prevent them from doing something with the keyboard), since they will make it impossible for keyboard-only users to access everything.

## Use the right HTML elements
Don't just put everything in a [[div]]. Use other elements like `<form>`, `<label>`, `<article>`, etc, to help support screen readers.

## Add skip links if required
Add a link that lets users skip to the main content to save them from needing to navigate through large amounts of content.

They can also be used to skip over infinite feeds (eg if there is a carousel view).