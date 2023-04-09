`useContext` is a [[React hook]] that allows you to share a global context across your entire app.

Create the global context
```jsx
// context.jsx
import React, { createCOntext } from 'react';

// Create default values
export const defaultValues = {
	userName: null,
	userToken: null,
};

// Create the context to be used
export const Context = createContext(initialValue);
// Handy so we are importing from the same spot, makes the relationship 
// more clear
export const useContext = React.useContext; 
```

Use the context provider in your app
```jsx
// Import the context so we can provide it in our app
import { Context, defaultValues } from './context';

const App = () => {
	// Initialise the state for each value
	// This is sorta repetitive and boiler-platey - is there a better way?
  const [userName, setUserName] = useState(defaultVales.userName);
  const [userToken, setUserToken] = useState(defaultValues.userToken);

	// And create objects for getters and setters
	const getters = {
	  userName,
	  userToken,
	};
	const setters = {
		setUserName,
		setUserToken,
	};
	return (
		// Provide the context by giving access to the getters and setters
		<Context.Provider value={{ getters, setters }}>
			<MainPage />
		</Context.Provider>
	);
}
```

Finally, use our context in a component
```jsx
import { useContext, Context } from './context';

const MainPage = () => {
  const { getters, setters } = useContext(Context);

	return (
		<>
			<p>Hello! You are logged in as {getters.userName}.</p>
		</>
	)
}
```