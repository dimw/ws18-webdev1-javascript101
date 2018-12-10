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

## Documentation
####  Operators
  - Comparison and equality operators
    - Comparison operators output true or false by comparing values.
    ```
    >, <, >=, <=, ===, and !==
    ```
  - Arithmetic operators
    - Arithmetic operators take numerical values (either literals or variables) as their operands and return a single numerical value.
    ```
    +, -, * and /
    ```
  - Logical operators
    - Logical operators combine multiple Booleans or Values and output a single boolean.
    ```
    &&, ||, and !
    ```
    
  _Source: [codeacademy/comparison_logical](https://www.codecademy.com/articles/fwd-js-comparison-logical) and [dev.moz/arithmetic_operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators)_

## Functions

### Function Declaration

##### Syntax:
````javascript
function sum(a, b) {
  return a + b;
}
````

A Function Declaration is usable in the whole script.
When JavaScript prepares to run the script or a code block, it first looks for Function Declarations in it and creates the functions.

Meaning, a function declared as a Function Declaration can be called earlier than it is defined.


For example:
```javascript
sayHi("John");

function sayHi(name) {
  alert( `Hello, ${name}` );
}
```
When a Function Declaration is made within a code block, it is visible everywhere inside that block. But not outside of it.

### Function Expression

##### Syntax:

```javascript
let sum = function(a, b) {
  return a + b;
};
```

A Function Expression is created when the execution reaches it and is usable from then on, but we can assign a function to a variable that is declared outside of a block.
 
For example:
````javascript
let age = prompt("What is your age?", 18);

let welcome;

if (age < 18) {

  welcome = function() {
    alert("Hello!");
  };

} else {

  welcome = function() {
    alert("Greetings!");
  };

}

welcome();
````
[Source: https://javascript.info/function-expressions-arrows]

#### Objects
 - `new` operator:
   - The new operator creates an instance of a user-defined object type or of one of the built-in object types that has a constructor function. The new keyword does the following 4 things: 
        1. It creates a brand new object out of thin air.
        2. It links this object to another object.
        3. The newly created object from Step 1 gets passed as the this context.
        4. If the function doesn't return it's own object, this is returned.
        
        ```
        function Car(make, model, year) {
                      this.make = make;
                      this.model = model;
                      this.year = year;
        }
                    
        var car1 = new Car('Eagle', 'Talon TSi', 1993);
           
        console.log(car1.make);
        // expected output: "Eagle"
        ```
         
   Source: [MDN new operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new)

