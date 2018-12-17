# JavaScript 101

## Contents
- Primitive typez
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
           - Declaration:
                    Man nimmt einen Wert und deklariert ihn mit var, let oder const
                    Var a = 5;
                        Resolves: Scopes `var`, `let`, `const`

           - Objects scope and this:
                    Scopes sind Funktionen oder Variablen in unserem Code abrufbar sind.
            function someFunc() {
                var _this = this;
                something.on("click", function() {
                    console.log(_this);
                });
            };

           - Function and Objects:
                    Über das Function -Objekt haben Sie Zugriff auf Eigenschaften einer JavaScript-Funktion.
                    New function(„Funktionsinhalt“,etc.)
  - Functions as objects
  - `new` operator
  - `call()` and `apply()`
- Prototypes
