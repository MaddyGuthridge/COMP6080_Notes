When writing web code you'll often need things to work asynchronously.

As such, we use event-driven programming.

## Running order
- Run through global scope in its entirety
- Enter event loop:
	- Check if there is any event that is ready
	- Run that event to completion
	- Repeat
	- If no events, wait for the next one to fire

NOTE:
Since each event is run to completion, it is possible to make the page unresponsive by doing a long-running calculation, which will prevent other events from being handled.

## Creating events
Events can be created in many ways

- User moved mouse
- User clicked something
- State of some element changed
- Timer finished
- etc etc etc

## Creating event listeners

Provide a [[callback]] function to be called on the event.

Listen for events on an HTML element
```js
someElement.addEventListener('event name', (ev) => {
  // Do stuff
});
```

Set a timeout
```js
setTimeout(() => {
  // Do stuff a second later
}, 1000)
```