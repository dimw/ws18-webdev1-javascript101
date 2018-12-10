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

##Functions as objects
The value of a key in an object can be a function.<br><br>Example:

        let dog = {
            bark: function() {
                alert("Wuff");
            }
        }
        let bark = dog.bark();
        
##'new' operator 
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
        
##call() 
A function (as a value) can be called with the object's name and the key.<br><br>Example:

        let dog = {
            name: 'Fluffy',
            greeting: 'Wuff',
            bark: function() {
                return this.greeting;
            }
        }
        let bark = dog.bark();
        
##apply() 
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
        
        adress.bark().apply(dog);