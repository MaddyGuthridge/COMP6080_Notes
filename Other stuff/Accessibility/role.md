Role properties are used to show the "role" that an element plays.

- `"alert"` - the user did something wrong, or something important happened
- `"progressbar"` - loading states, eg file uploads
- `"status"` - changes of status (eg a new item becomes available)
- `"log"` - notifications and chat messages
- `"timer"` - count-downs and stop-watches

By default, only the changes are announced. To announce everything each time (useful for timers), use `aria-atomic={true}`

For announcements, you can use the `aria-live` property to interrupt the user.
