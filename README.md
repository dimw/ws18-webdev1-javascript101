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

## Functions as objects
The value of a key in an object can be a function.<br><br>Example:

        let dog = {
            bark: function() {
                alert("Wuff");
            }
        }
        let bark = dog.bark();
        
## 'new' operator 
An object can be created with a constructor-method.<br><br>Example:

        class dog {
                constructor (breed, age, name, castrated) {
                    this.breed = breed;
                    this.age = age;
                    this.name = name;
                    this.castrated = castrated;
                }
        }
        let newDog = new dog('Rodweiler', 3, 'Fluffy', true);
        
## call() 
A function (as a value) can be called with the object's name and the key.<br><br>Example:

        let dog = {
            name: 'Fluffy',
            greeting: 'Wuff',
            bark: function() {
                return this.greeting;
            }
        }
        let bark = dog.bark();
        
## apply() 
A function (as a value) can be applied to other external class objects.<br><br>Example:

        let address = {
            bark: function() {
                return this.greeting;
            }
        }
        let dog = {
            name: 'Fluffy',
            greeting: 'Wuff'
        }
        
        address.bark().apply(dog);