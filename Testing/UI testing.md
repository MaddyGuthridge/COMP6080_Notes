UI testing is the process of [[testing]] [[user interface|user interfaces]] to ensure that it is working correctly. It is a kind of [[integration testing]].

## When to write UI tests
- Always cover the "happy path" (where we want to be sure that it is working correctly).
- We don't always need to cover other paths, but if they are common, we should do so.

## How UI testing works
There are various strategies we can use to test a UI

### Fake DOM
We can create a fake [[DOM]], which will let us quickly test things, but isn't as fully-featured as a real web browser.

For example: [jsdom](https://www.npmjs.com/package/jsdom)

### Browser automation
We can also automate a web browser by using a Webdriver, which allows us to programmatically control a web browser.

Examples:
- [Selenium](https://www.selenium.dev/)

## Locators
A locator is used to locate elements within the DOM.
- By CSS ID
- By CSS class name
- By `name` attribute
- By [[HTML]] tag name
- By link text
- By partial link text
- By xpath