[Redux](https://redux.js.org/) is a [[JavaScript]] library to keep track of a global [[state management]]. It's almost definitely much better than [[local storage]]. For simpler tasks, you could still consider using a [[useContext]] hook with some persistence added in.

Redux is built using a [[store]], which then has [[action|actions]] and [[reducer|reducers]] to modify it.

## Benefits
### Debuggable
Redux can track all changes to the state, allowing you to "time travel" and see what your app did to get itself into an invalid state.

### Easy caching and persistence
Yayyyy no more local storage!
