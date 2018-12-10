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

## Control Structures
### If - Else If - Else
#### General Structure
```js
if (condition1) {
     //when condition1 is true this will be executed
   } else if (condition2) {
     //if condition1 is false and condition2 is true this will be executed is true
   } else {
     //this will be executed if condition1 and condition2 are false
   }
```

#### Example
   
```js
   let name = 'peter';
   if (name === 'max') {
        console.log('If was true')
      } else if (name === 'peter') {
        console.log('Else if was true')
      } else {
        console.log('Else was true')
      }
```

###### Console
   
```bash
  Else if was true
```

### Switch
#### General Structure
```js
switch (ValueToSwitch) {
     case firstValueToCompare:
       //This will run if ValueToSwitch == firstValueToCompare
       break;
     case secondValueToCompare:
      //This will run if ValueToSwitch == secondValueToCompare
       break;
}
```

#### Example
   
```js
	let day = ""
   switch ("Peter Parker") {
     case 0:
       day = "Monday";
       break;
     case 1:
        day = "Tuesday";
       break;
     case 2:
       day = "Wednesday";
       break;
     case 3:
       day = "Thursday";
       break;
     case 4:
       day = "Friday";
       break;
     case 5:
       day = "Saturday";
       break;
     case 6:
      	day = "Sunday";
      	break;
     default:
     	day = "This is not a week day"
   }
   console.log(day)
```

###### Console
   
```bash
  This is not a week day
```

### For Loop
#### General Structure
```js
let i;
for (i = 0; i < Array.length; i++) {
  //This will run while i is smaller then the Array
  //With each iteration i will increase by one
}
```

#### Example
   
```js
let text = ""
for (let i = 0; i < 5; i++) {
  text += "The number is " + i + "\n";
}
console.log(text)
```

###### Console
   
```bash
  The number is 0
  The number is 1
  The number is 2
  The number is 3
  The number is 4
```

### While and Do While
#### General Structure

```js
while (condition) {
  //the code while run while condition is true
   //The check runs before the first iteration
}
```

```js
do {
  //the code while run while condition is true
  //The check runs after the first iteration
}
while (condition);
```

#### Example
   
```js
let i = 0;
let text = "";
while (i < 10) {
  text += "The number is " + i + "\n";
  i++;
}
console.log(text)
```

###### Console
   
```bash
	The number is 0
	The number is 1
	The number is 2
	The number is 3
	The number is 4
	The number is 5
	The number is 6
	The number is 7
	The number is 8
	The number is 9
```

##  Operators
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

## Objects
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

