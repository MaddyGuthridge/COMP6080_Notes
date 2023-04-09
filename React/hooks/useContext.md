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

// Create the context to be us
export const Context = createContext(initialValue);
// Handy so we are importing from the same spot, makes the relationship 
// more clear
export const useContext = React.useContext; 
```

Use the context provider in your main page
```jsx
import { Context, defaultValues } from './context';

const App = () => {
  const [userName, setUserName] = useState(defaultVales.userName);
  const [userToken, setUserToken] = useState(defaultValues.userToken);

	const getters = {
	  userName,
	  userToken,
	};
	const setters = {
		setUserName,
		setUserToken,
	};
	return (
		<Context.Provider value={{ getters, setters }}>
			<MainPage />
		</Context.Provider>
	);
}
```

Finally