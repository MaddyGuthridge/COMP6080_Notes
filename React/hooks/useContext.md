`useContext` is a [[React hook]] that allows you to share a global context across your entire app.

Create the global context
```jsx
// context.jsx
import React, { createCOntext } from 'react';

export const defaultValues = {
	userName: null,
	userToken: null
}
```

Use the context provider in your main page
```jsx
import { Context } from './context'; // what is this?

const App = () => {
  const [userName, setUserName] = useState(0);
  const [userToken, setUserToken] = useState(null);

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