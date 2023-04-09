`useContext` is a [[React hook]] that allows you to share a global context across your entire app.

```jsx
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