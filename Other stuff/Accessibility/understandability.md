For a webpage needs to be understandable, it needs to be created in a way so that it can be understood by anyone.

## Defining the language

```html
<html lang="en">
  ...
</html>
```
Very helpful for screen readers

## Keeping things consistent
Don't change the underlying [[HTML]] unless the content is changing. Don't change IDs of elements.

## Making it work with partial downloads
The page should at least look somewhat readable without CSS

## Making it indexable
You should give your pages proper metadata in the HTML [[head]].
- `<title>`
- `<meta>`
	- `name="description" content="A description of the website"`

## Making links understandable
Link should be understandable in the context of the sentence at a minimum. Optimally, it should be understandable by itself.
- "I understand the terms of service `<br><br>` [click here](https://www.youtube.com/watch?v=dQw4w9WgXcQ)" = bad
- "I understand the terms of service, available [here](https://www.youtube.com/watch?v=dQw4w9WgXcQ)" - decent
- "I understand the [terms of service](https://www.youtube.com/watch?v=dQw4w9WgXcQ)" - great!

## Properly label form elements
Best practice:
```html
<label for={someInput}>Name</label>
<input id={someInput} />
```

Alternate best-practice, using [[ARIA]]:
```html
<label id={someLabel}>Name</label>
<input aria-labelledby={someLabel} />
```

Or if you're not giving a visible label:
```html
<input aria-label="Name" />
```

Passable, but can break if you're using custom components:
```html
<label>
	Name
	<input />
</label>
```

**Don't use placeholder text by itself** - it doesn't work with screen readers.

### Field descriptions
You can also associate longer content such as error messages with an input.
```html
<label for={someInput}>Name</label>
<input
	id={someInput}
	aria-describedby={someDescription}
/>
<p id={someDescription} role="alert">
	Some error message to do with the input field
</p>
```

Notice the use of the [[role]] to show that the error message should be immediately announced to users.

You can also use other properties to help out with field validation:
- `required` - mark a field as required
- `type="number" min={0}` - set the minimum value for a number input
- `type="password" minLength={8}` - set the minimum length for a text input

For other kinds of form mistakes, set `aria-invalid` to `{true}` and set `aria-describedby` to the ID of an error message.