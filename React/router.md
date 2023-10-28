Using the `react-router-dom` package, you can create a "router", which allows you to conditionally render various pages.

```jsx
import {
	BrowserRouter,
	Routes,
	Route,
} from 'react-router-dom';

function App() {
	return (
		<>
			<BrowserRouter>
				<Routes>
					<Route path="/" element={<Home />} />
					<Route path="/about" element={<About />} />
				</Routes>
			</BrowserRouter>
		</>
	)
}
```

### Nested routes
```jsx
import {
	BrowserRouter,
	Routes,
	Route,
} from 'react-router-dom';

function App() {
	return (
		<>
			<BrowserRouter>
				<Routes>
					<Route path="/" element={<Home />} />
					{/* 
					  * Note that the About element is rendered for both the sub routes
					  * It must include an `<Outlet>` component in order to allow those 
					  * sub-pages to render within the <Outlet> element
					  */}
					<Route path="/about" element={<About />}>
						<Route path="me" element={<AboutMe />}>
						<Route path="you" element={<AboutYou />}>
					</Route>
				</Routes>
			</BrowserRouter>
		</>
	)
}
```

## Changing between routes

To link to a different route
```jsx
import { Link } from 'react-router-dom';

function LinkThing() {
  <Link to="/">Go to the homepage</Link>
}
```

Note that our `LinkThing` [[component]] must be contained within the `BrowserRouter` element, otherwise it can't change the page.

### Why not `<a>`

Using an [[anchor]] tag would trigger a full reload.

### As a function

To change between routes using a function, you can use the `useNavigate` hook
```jsx
import { useNavigate } from 'react-router-dom';
function MyComponent() {
	const navigate = useNavigate();
	return (
		<button onClick={() => navigate("/about") }>About page</button>
	);
}
```

## Wildcard elements

Add a `:` before a wildcard element in a route. Then use the `useParams` hook to grab the parameters from the route inside the element.

```jsx
<Route path="/video/:videoId" element={<WatchPage />} />
```

And in the element
```jsx
import { useParams } from 'react-router-dom';
function WatchPage() {
  const params = useParams();

	return (
		// This probably doesn't work like this I just wanted the example
		<Video path={`https://backend.mysite.com/content/${params.videoId}.mp4`} />
	)
}
```

Then the user can visit `https://mysite.com/video/dQw4w9WgXcQ` and enjoy the video.
