JSX (***J*avaScript *S*yntax e*X*tension**, or ***J*ava*S*cript *X*ML**, depending on who you ask) is a system for embedding [[HTML]] inside [[JavaScript]] code. It's used by [[React]] to create [[component|components]].

It gets [[transpilation|transpiled]] to regular JS, usually with WebPack.

### Comments inside JSX HTML

```jsx
function MyComponent() {
  return (
	  <>
		  {/**
		    * This is a comment
		    * The syntax is gross
		    */}
	  </>
  );
}
```
