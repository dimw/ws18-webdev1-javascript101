# JavaScript 101

## Contents
- Primitive types  
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
  - Callback pattern & pass function as parameter
  - Call by value vs. call by reference
- Objects
  - Declaration
  - Object scope and `this`
  - Functions and objects
  - Functions as objects
  - `new` operator
  - `call()` and `apply()`
- Prototypes

## Documentation

### Primitive types
Is data that is not an object and has no methods.
  - `Number` : JavaScript has only one type of numbers. Numbers can be written with, or without decimals
  - `Boolean` : Boolean represents a logical entity and can have two values: true, and false
  - `String` : JavaScript's String type is used to represent textual data. It is a set of "elements" of 16-bit unsigned integer values. 
  - `Array` : Arrays are regular objects for which there is a particular relationship between integer-key-ed properties and the 'length' property.
  - `Type conversion` : Number() converts to a Number, String() converts to a String, Boolean() converts to a Boolean, parseInt()	Parses a string and returns an integer.

  ### [Scopes](https://developer.mozilla.org/en-US/docs/Glossary/Scope)

  The current context of execution. The context in which values and expressions are "visible," or can be referenced. If a variable or other expression is not "in the current scope," then it is unavailable for use. Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.
  - **`var`, `let`, `const` – variable types**
    - `var`: Globally scoped or function/locally scoped, can be re-declared and updated
    - `let`: Preferred for variable declaration now, block-scoped, can be updated but not re-declared.
    - `const`: Maintain constant values. const declarations share some similarities with let declarations. cannot be updated or re-declared
  - [**Callback pattern & pass function as parameter:**](https://developer.mozilla.org/en-US/docs/Glossary/Callback_function)

    A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.
    ```javascript
    function greeting(name) {
        alert('Hello ' + name);
    }

    function processUserInput(callback) {
        var name = prompt('Please enter your name.');
        callback(name);
    }

    processUserInput(greeting);
    ```
  - [**Call by value vs. call by reference**](https://stackoverflow.com/questions/6605640/javascript-by-reference-vs-by-value)
  
    Javascript always passes by value. However, if you pass an object to a function, the "value" is really a reference to that object, so the function can modify that object's properties but not cause the variable outside the function to point to some other object.