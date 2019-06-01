---
tags: javascript
source: http://tc39wiki.calculist.org/es6/arrow-functions/
---
arrow functions are roughly the equivalent of lambda functions in python or blocks in Ruby.

An arrow function expression is a syntactically compact alternative to a regular function expression, although without its own bindings to the this, arguments, super, or new.target keywords. Arrow function expressions are ill suited as methods, and they cannot be used as constructors.

The goal of Arrow Functions is to address and resolve several common pain points of traditional `Function` Expression: 
pros:

* Lexical this binding;

* Shorter syntactical form (() => {} vs. function () {})
