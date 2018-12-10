# JavaScript 101

## Contents
- Primitive types
  - Number
  - Boolean
  - String
  - Array
  - Type conversion
- Operators
  - Comparison and equality operators
  - Arithmetic operators
  - Logical operators
- Control Structures
  - `if ... else if ... else ...`
  - `switch`
  - `for` loop
  - `while` and `do while` loops
- Functions
  - Declaration
  - Call
  - Function hoisting
  - Anonymous self-invoking function
  - Optional parameters
  - Arguments array
  - Recursion
  - Lambda notation
- Scopes
  - `var`, `let`, `const`
  - Pass function as parameterr
  - Callback pattern
  - Call by value vs. call by reference
- Objects
  - Declaration
  - Object scope and `this`
  - Functions and objects
  - Functions as objects
  - `new` operator
  - `call()` and `apply()`
- Prototypes

## Functions

### Function hoisting

Functions hoisting is best explained by looking at this example:

> First we call `multiply()`

```javascript
multiply(2, 4)
```

> And later in the same file, we declare `multiply()`

```javascript
function multiply(a, b) {
    return a * b;
}
```

In the example, we see that the function `multiply` is called, before it was declarated. And we wouldn't even get any errors with this approach. This is, because the JavaScript interpreter "looks ahead" and moves function declarations to the top of the file. **BUT** this is only the case for function declarations, like the one above. **NOT** for function expression, like the following:

> In a new file, let's call `multiply()`

```javascript
multiply(2, 4);
```
> `Output: 8`<br/><br/>
> And then call a new function `divide()`

```javascript
divide(2, 4); 
```

> `Output: TypeError: undefined is not a function` <br/><br/>
> And next we're gonna declare both of the functions.

```javascript
function multiply(a, b) { /* Nerdy math crap */ }
var divide = function (a, b) { /* More nerdy math crap */ }
```

> We see, multiply is function declarationg and divide is a function expression, as it's an anonymous function assigned to a variable.

__TL;DR__: Traditional function declaration can be called before the function declaration. This __only__ works with function declarations, not expressions like assigning an anonymous function to a variable.

[Source](http://adripofjavascript.com/blog/drips/variable-and-function-hoisting.html)

### Anonymous self-invoking functions

Sometimes we need to initialize event-listeners, or generally perform any actions that are only required once, after the page loaded. For this we can use anonymous self-invoking functions. As the name states, the function is anonymous and executed right after it's declaration.<br/>
Let's jump into an example:

```javascript
(function(w, d, $) {
    // Some programmatic fuckery 
})(window, document, jQuery);
```

> The function above will be executed with `window`, `document`, and `jQuery` as it's parameters. Inside the function, we can access the paramers as `w`, `d` and `$`.

[Source](https://blog.mgechev.com/2012/08/29/self-invoking-functions-in-javascript-or-immediately-invoked-function-expression/)