Declarative UI frameworks aim to describe what a UI looks like, rather than how to create it.

## Problems to solve
Declarative UIs aim to solve the following problems
### Increasing complexity
By specifying the end result, we don't need to worry about handling the edge cases - React will sort it out for us.
### Untracked UI Mutations
By writing declaratively, we can ensure that we don't accidentally forget to add/remove elements during transitions.

## Virtual DOM
[[React]] uses a "virtual [[DOM]]" to allow for efficient updates. It renders the new DOM, then calculates the diff with the current DOM, then only makes the required changes to get from the old state to the new state.