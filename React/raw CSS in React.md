In [[React]], we need to explicitly import [[CSS]], which would make you think that the CSS is limited in scope, ***BUT NO!!!*** Any CSS you import is available globally. Prepare for the same CSS namespace pollution pains you're used to from raw HTML.

To style an element
```jsx
// Import the CSS explicitly
import './App.css'

function MyComponent() {
  return (
	  <div className="my-component-class">
	    Wow this text is fancy and stylish
	  </div>
  )
}
```

To fix this awfulness, you'll want to use a [[component library]] and [[styled component|styled components]].