[[single-page app|Single-page apps]] are terrible for [[search engine optimisation]], since web crawlers can't see all the content. To fix this, we can pre-render our pages to only contain the bare minimum HTML to display the page. We can then load the JS to make our app interactive in a process called "hydration".

## Static site generation
For a static site, it makes it much faster to load. We pre-render our code into [[HTML]] at build-time so it can be distributed over a CDN.

There are ways to populate it later if needed.

Don't use it if your data is updating frequently

## Server-side rendering
Render the page on the server.