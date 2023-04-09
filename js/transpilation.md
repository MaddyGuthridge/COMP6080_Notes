Lots of code in web development is transpiled, meaning it is converted from one language to another. This is usually done to ensure compatibility with older browsers, or to allow for other features to be used (such as [[JSX]]). The most common target for transpilation in web development is [[JavaScript]].

## Polyfills
Tools like [Core-JS](https://github.com/zloirock/core-js) can be used to create "polyfills", which monkey-patch in any required functions to the JS standard library in order to support new features in old browsers.

## Transformers
Tools like [Babel](https://github.com/babel/babel) can be used to transform new syntax (eg [[async-await]], and [[promises]]) into old syntax (eg [[callback|callbacks]]).

## JS flavours
There are many other flavours of JS that allow for other features to be transpiled to JavaScript, such as [TypeScript](https://www.typescriptlang.org/) and CoffeeScript.

## Minification
Rewriting code to reduce the number of bytes (shortening variable names, removing comments, etc).

Eg [Google's Closure Compiler](https://developers.google.com/closure/compiler/)

## Obfuscation
Making the code super confusing so it's harder for people to reverse-engineer it.

## Build tools
Build tools take code and perform the required transpilation, then bundle up the code to make it as small as possible.