Component testing is the process of [[testing]] that a component is working correctly. It is a type of [[unit testing]].

```jsx
// Import functions for rendering elements and checking their output
import { render, screen } from '@testing-library/react';
// Import function for simulating user interaction
import userEvent from '@testing-library/user-event';
// Import the element we want to test
import { Button } from './Button';

describe('<Button />', () => {
	it('renders correctly', () => {
		// Render the button
		render(<Button />);
		// Make sure it appears in the DOM
		expect(
			// Get an element by its role, with the given properties
			screen.getByRole('button', { name: /click me!/i })
		).toBeInTheDocument();

		// We can print out the contents of the dom using
		screen.debug();
		
		// And we can also generate a link to testing-playground.com
		// where we can interactively select elements (neat!)
		screen.logTestingPlaygroundURL();
	});
});
```

## Getting elements
Try this order
- `getByRole` - this ensures it is working for [[accessibility]]
- other [[selectors]] (idk what they are the lectures didn't say)