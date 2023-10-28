Static site generation (SSG) is the act of [[pre-rendering]] our code into [[HTML]] at build-time so it can be distributed over a CDN.

There are ways to populate it later if needed.

Don't use it if your data is updating frequently, since it'll be painful to keep it up-to-date (consider [[server-side rendering|SSR]] instead).
