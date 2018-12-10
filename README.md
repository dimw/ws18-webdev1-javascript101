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

##Documentation
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
