
# JavaScript Tutorial

This tutorial covers essential JavaScript concepts to help you get started or enhance your understanding.

---

## 📋 Index

1. [Variables](#1-variables)
2. [Operators](#2-operators)
3. [Data Types](#3-data-types)
4. [Functions](#4-functions)
5. [Loops](#5-loops)
6. [Objects](#6-objects)
7. [Error Handling](#7-error-handling)

---

## 1. Variables

In JavaScript, variables store data values. You can declare variables using `var`, `let`, or `const`.In a programming language, variables are used to store data values.JavaScript uses the keywords var, let and const to declare variables.
An equal sign is used to assign values to variables.

### Example using `let`:

```javascript
let a = 4;
let b = 5;
console.log(a ** b); // 4^5
```

### Example using `const`:

```javascript
const x = 5;
const y = 6;
const z = x + y;
```

Value = undefined

In computer programs, variables are often declared without a value. The value can be something that has to be calculated, or something that will be provided later, like user input.Variables declared without an initial value have the value `undefined`.

```javascript
let carName;
console.log(carName); // undefined
```

### Variable Rules

- **`let` and `const`**: Cannot be redeclared.
- **`const`**: Cannot be reassigned and has block scope. Use `const` by default, unless you need to reassign.

With let you can not do this:
```Let
let x = "John Doe";
let x = 0;
```
But with var you can do this.As a general rule, always declare a variable with const unless you know that the value will change.

![image](https://github.com/user-attachments/assets/547c2125-90af-417d-85c3-bfd8a9637d2b)


---

## 2. Operators

JavaScript uses different operators to perform calculations, comparisons, and other operations.

### Arithmetic Operators

```javascript
let x = 5;
let y = 2;
let z = x % y; //  1
```

### Assignment Operators


| Operator | Description                     | Example             | Equivalent Expression    |
|----------|---------------------------------|---------------------|--------------------------|
| `=`      | Assigns right-hand value to left-hand variable | `x = 5`           | `x = 5`                  |
| `+=`     | Adds and assigns               | `x += 2` (same as `x = x + 2`) | `x = x + 2`              |
| `-=`     | Subtracts and assigns          | `x -= 2` (same as `x = x - 2`) | `x = x - 2`              |
| `*=`     | Multiplies and assigns         | `x *= 2` (same as `x = x * 2`) | `x = x * 2`              |
| `/=`     | Divides and assigns            | `x /= 2` (same as `x = x / 2`) | `x = x / 2`              |
| `%=`     | Modulus and assigns            | `x %= 2` (same as `x = x % 2`) | `x = x % 2`              |
| `**=`    | Exponentiation and assigns     | `x **= 2` (same as `x = x ** 2`) | `x = x ** 2`             |
| `<<=`    | Left shift and assigns         | `x <<= 2` (same as `x = x << 2`) | `x = x << 2`             |
| `>>=`    | Right shift and assigns        | `x >>= 2` (same as `x = x >> 2`) | `x = x >> 2`             |
| `&=`     | Bitwise AND and assigns        | `x &= 2` (same as `x = x & 2`) | `x = x & 2`              |
| `|=`     | Bitwise OR and assigns         | `x |= 2` (same as `x = x | 2`) | `x = x | 2`              |
| `^=`     | Bitwise XOR and assigns        | `x ^= 2` (same as `x = x ^ 2`) | `x = x ^ 2`              |

- JavaScript uses an assignment operator ( = ) to assign values to variables:


```javascript
let text = "Hello";
text += " World"; // Hello World
```
### Simple Assignment and Chaining:


```
let x = 5;
let y = 10;
let z = 25;

x = y; // x is 10
x = y = z; // x, y and z are all 25
```


The assignment expression itself evaluates to the value of the right-hand side, so you can log the value and assign to a variable at the same time.



```
let x;
console.log(x); // undefined
console.log(x = 2); // 2
console.log(x); // 2
```

### JavaScript Comparison Operators

| Operator| Name                   | Description                                                                 | Example             |
|----------|-------------------------|-----------------------------------------------------------------------------|---------------------|
| `==`     |  Equality                | Checks if values are equal after type coercion.                             | `5 == "5"` → `true` |
| `===`    | Strict Equality         | Checks if values and types are equal without type coercion.                 | `5 === "5"` → `false`|
| `!=`     | Inequality              | Checks if values are not equal after type coercion.                         | `5 != "5"` → `false`|
| `!==`    | Strict Inequality       | Checks if values and types are not equal without type coercion.             | `5 !== "5"` → `true` |
| `>`      | Greater Than            | Checks if the left value is greater than the right.                         | `5 > 3` → `true`    |
| `<`      | Less Than               | Checks if the left value is less than the right.                            | `5 < 3` → `false`   |
| `>=`     | Greater Than or Equal   | Checks if the left value is greater than or equal to the right.             | `5 >= 5` → `true`   |
| `<=`     | Less Than or Equal      | Checks if the left value is less than or equal to the right.                | `5 <= 3` → `false`  |


- `==` checks for equality with type coercion.
- `===` checks for equality without type coercion. Recommended for accurate comparisons.

- == (Equality Operator):This operator checks for equality after performing type coercion. It converts the operands to the same type before making the comparison.For example, 5 == "5" would be true because the string "5" is coerced to the number 5 during the comparison.
- === (Strict Equality Operator):This operator checks for equality without performing type coercion. It compares both the value and the type of the operands.For example, 5 === "5" would be false because the value 5 is of type number, and the string "5" is of type string.

In general, it is recommended to use === (strict equality) to avoid unexpected results due to type coercion. Using === ensures that both the value and the type are the same for the comparison to be true.

### Logical Operators

```javascript
const a = 3;
const b = -2;
console.log(a > 0 && b > 0); // false
console.log(!(a > 0 || b > 0)); // false
```

### Bitwise Operators


| Operator | Name          | Description                                                                                           | Example                    |
|----------|---------------|-------------------------------------------------------------------------------------------------------|----------------------------|
| `&`      | AND           | Performs a bitwise AND operation; sets each bit to `1` if both bits are `1`.                         | `5 & 3` → `1`              |
| `|`      | OR            | Performs a bitwise OR operation; sets each bit to `1` if at least one of the bits is `1`.            | `5 | 3` → `7`              |
| `^`      | XOR           | Performs a bitwise XOR operation; sets each bit to `1` only if one of the bits is `1`, not both.     | `5 ^ 3` → `6`              |
| `~`      | NOT           | Inverts all bits; flips each bit, turning `1`s to `0`s and `0`s to `1`s.                            | `~5` → `-6`               |
| `<<`     | Left Shift    | Shifts bits to the left by specified number of positions, adding `0`s on the right.                   | `5 << 1` → `10`           |
| `>>`     | Right Shift   | Shifts bits to the right by specified number of positions, preserving the sign bit (signed shift).    | `5 >> 1` → `2`            |
| `>>>`    | Zero-fill Right Shift | Shifts bits to the right by specified positions, filling the left with `0`s (unsigned shift). | `5 >>> 1` → `2`           |


Example of signed and unsigned right shifts:

```javascript
let x = -8;
console.log(x >> 2);   // -2 (Signed right shift)
console.log(x >>> 2);  // 1073741822 (Unsigned right shift)
```
>> (Signed Right Shift):
The >> operator shifts the bits of a number to the right. It preserves the sign bit, which means that if the number is positive, it pads the left side with zeros, and if the number is negative, it pads the left side with ones.
Example: x >> y shifts the bits of x to the right by y positions.
>>> (Unsigned Right Shift):
The >>> operator also shifts the bits to the right, but it always pads the left side with zeros, regardless of the sign of the number. It treats the number as if it were an unsigned integer.
Example: x >>> y shifts the bits of x to the right by y positions, and the left side is always padded with zeros.
Here's a quick example to illustrate the difference:
Bitwise XOR:


The bitwise XOR (^) operator returns a number or BigInt whose binary representation has a 1 in each bit position for which the corresponding bits of either but not both operands are 1.

```
const a = 5;
const b = 3; 

console.log(a ^ b);
// Expected output: 6
```
### Conditional (Ternary) Operator
The conditional (ternary) operator is the only JavaScript operator that takes three operands: a condition followed by a question mark (?), then an expression to execute if the condition is truthy followed by a colon (:), and finally the expression to execute if the condition is false. This operator is frequently used as an alternative to an if...else statement

```javascript
let age = 18;
let result = age > 18 ? "adult" : "notAdult";
console.log(result); // notAdult
```
### JavaScript String Operators:


JavaScript String Operators are used to manipulate and perform operations on strings. There are two operators which are used to modify strings in JavaScript. These operators help us to join one string to another string.


##### Type of JavaScript String Operators:




##### 1. Concatenation (+ Operator)


The + operator is used to join two or more strings together.

```
let greeting = "Hello, " + "world!";  //  "Hello, world!"
```

##### 2. Concatenation Assignment (+= Operator)

   
The += operator appends one string to another and assigns the result to the original variable.
```
let message = "Hello";
message += ", world!"; // message becomes "Hello, world!"
```
### `typeof` Operator in JavaScript

The `typeof` operator is used to check the data type of a variable or value in JavaScript.
A complex data type can store multiple values and/or different data types together.
JavaScript has one complex data type:
- object

All other complex types like arrays, functions, sets, and maps are just different types of objects.



| Value                  | Expression         | Output       | Description                               |
|------------------------|--------------------|--------------|-------------------------------------------|
| `"Hello"`              | `typeof "Hello"`   | `"string"`   | String data type                          |
| `42`                   | `typeof 42`        | `"number"`   | Number data type                          |
| `true`                 | `typeof true`      | `"boolean"`  | Boolean data type                         |
| `undefined`            | `typeof undefined` | `"undefined"` | Undefined data type                     |
| `Symbol("id")`         | `typeof Symbol("id")` | `"symbol"` | Symbol data type                          |
| `9007199254740991n`    | `typeof 9007199254740991n` | `"bigint"` | BigInt data type                     |
| `null`                 | `typeof null`      | `"object"`   | Null (historically returns "object")      |
| `{ name: 'John' }`     | `typeof { name: 'John' }` | `"object"` | Object data type                         |
| `[1, 2, 3, 4]`         | `typeof [1, 2, 3, 4]` | `"object"` | Array (treated as object)                |
| `new Map()`            | `typeof new Map()` | `"object"`   | Map (treated as object)                  |
| `new Set()`            | `typeof new Set()` | `"object"`   | Set (treated as object)                  |
| `function() {}`        | `typeof function() {}` | `"function"` | Function data type                    |




### The instanceof Operator

The instanceof operator returns true if an object is an instance of a specified object type:
```

const time = new Date();

(time instanceof Date);  //Date:True

```
```
const myArray = [1, 2, 3];
console.log(myArray instanceof Array);    // true
console.log(myArray instanceof Object);   //  true
console.log(myArray instanceof Date);     //  false
```
---

## 3. Data Types
JavaScript variables can hold numbers like 100 and text values like "John Doe".In programming, text values are called text strings.JavaScript can handle many types of data, but for now, just think of numbers and strings. Strings are written inside double or single quotes. Numbers are written without quotes.If you put a number in quotes, it will be treated as a text string.

JavaScript has the following data types:

- **Primitive**: `String`, `Number`, `BigInt`, `Boolean`, `Undefined`, `Null`, `Symbol`
- **Complex**: `Object` (e.g., arrays, functions, maps, sets)
```
// Numbers:
let length = 16;
let weight = 7.5;

// Strings:
let color = "Yellow";
let lastName = "Johnson";

// Booleans
let x = true;
let y = false;

// Object:
const person = {firstName:"John", lastName:"Doe"};

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");

//Symbol :
let symbol1 = Symbol("Khan")
let symbol2 = Symbol("Khan")
  
// Each time Symbol() method  is used to create new global Symbol
console.log(symbol1 == symbol2); // False (because symbols are always unique)
```
When adding a number and a string, JavaScript will treat the number as a string.
```
let x = "5" + "world";
```
---

## 4. Functions
A JavaScript function is a block of code designed to perform a particular task.It is executed when "something" invokes it (calls it).
```
// Function to compute the product of p1 and p2
function myFunction(p1, p2) {
  return p1 * p2;
}
```
#### JavaScript Function Syntax
- A JavaScript function is defined with the function keyword, followed by a name, followed by parentheses ().
- Function names can contain letters, digits, underscores, and dollar signs (same rules as variables).
- The parentheses may include parameter names separated by commas:(parameter1, parameter2, ...)
- The code to be executed, by the function, is placed inside curly brackets: {}
- Function parameters are listed inside the parentheses () in the function definition.
- Function arguments are the values received by the function when it is invoked.
- Inside the function, the arguments (the parameters) behave as local variables.
```
function name(parameter1, parameter2, parameter3) {
  // code to be executed
}
```
#### Function Invocation
- The code inside the function will execute when "something" invokes (calls) the function:
- When an event occurs (when a user clicks a button)
- When it is invoked (called) from JavaScript code
- Automatically (self invoked)
#### Function Return
- When JavaScript reaches a return statement, the function will stop executing.
- If the function was invoked from a statement, JavaScript will "return" to execute the code after the invoking 
  statement.
- Functions often compute a return value. The return value is "returned" back to the "caller":


Functions define reusable blocks of code.

#### Function Types

- **Normal Function**:
 ```
 function countvowel(str){
    let c=0;
    for(const char of str){
        if(char=="a"||char=="e"||char=="i"||char=="o"||char=="u"){
            c++;
        }
    }
    console.log(c);
}
countvowel("i am a girl");

  ```

- **Arrow Function**:
 ```javascript
const arrowmul = (a,b) => {
    return a*b;
};
  ```

- **Bind Function**:
  ```javascript
  let obj = { x: 5 };
  function getX() { return this.x; }
  let boundGetX = getX.bind(obj);
  ```

---

## 5. Loops

Loops are used to repeat code.
#### The For Loop
The for statement creates a loop with 3 optional expressions:
```
for (expression 1; expression 2; expression 3) { // code block to be executed}
```
**Expression 1** is executed (one time) before the execution of the code block.
**Expression 2** defines the condition for executing the code block.
**Expression 3** is executed (every time) after the code block has been executed.


  ```javascript
 let arr=[1,2,3,4,5]
for(let i=0;i<arr.length;i++){
    console.log(arr[i]);
 }
  ```
##### For of
```
let item =[10,20,30,40];
let i=0;
for(let val of item){
    console.log(`value at index ${i}=${val}`);
    let offer=val/10;
    item[i]=item[i]-offer;
    console.log(`after offer ${item[i]}`)
    i++;
}
```
```
//Output:
value at index 0=10
java.js:40
after offer 9
java.js:43
value at index 1=20
java.js:40
after offer 18
java.js:43
value at index 2=30
java.js:40
after offer 27
java.js:43
value at index 3=40
java.js:40
after offer 36
```
##### For in
```
const person = {fname:"John", lname:"Doe", age:25};

let text = "";
for (let x in person) {
  text += person[x]; //John Doe 25
}
```
#### while loop:
- **The while loop loops through a block of code as long as a specified condition is true.**
```
while (condition) { // code block to be executed}
````

  ```javascript
  let i = 0;
  while (i < 5) {
    console.log(i);
    i++;
  }
  ```

---

## 6. Objects
You have already learned that JavaScript variables are containers for data values.Objects are variables too. But objects can contain many values. This code assigns many values (Fiat, 500, white) to a variable named car:The values are written as name:value pairs (name and value separated by a colon).

```
const car = {type:"Fiat", model:"500", color:"white"};
```
#### Creating an Object
```
const student={
    name:"shifa",
    ispresent:true,
};
let output=`My name is ${student.name} \npresent is ${student.ispresent}`
console.log(output);

// My name is shifa
// present is true
```
Objects can also have methods.Methods are actions that can be performed on objects.Methods are stored in properties as function definitions.A method is a function stored as a property.

#### Creating an Object with Method
```
const person = {
  firstName: "John",
  lastName: "Doe",
  id: 5566,
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
```
#### Accessing Object Methods
objectName.methodName()
- name = person.fullName();





---

## 7. Error Handling

Use `try...catch` to handle errors gracefully.

```javascript
try {
  let result = riskyOperation();
} catch (error) {
  console.log("An error occurred:", error.message);
} finally {
  console.log("Execution completed");
}
```
Traditionally, JavaScript uses try-catch blocks to handle errors, especially in functions that involve async operations. But when you have multiple layers of try-catch, the code quickly becomes complex, hard to read, and harder to maintain.
```
async function fetchData() {
    try {
        const response = await fetch("https://api.example.com/data");

        if (!response.ok) {
            throw new Error(`Network response was not ok: ${response.statusText}`);
        }

        const data = await response.json();
        return data;

    } catch (error) {
        if (error instanceof SyntaxError) {
            console.error('Failed to parse JSON:', error);
        } else {
            console.error('Network request failed:', error);
        }
    }
}
```

#### The Solution: The ?= Operator
The new ?= operator provides a simple and effective alternative. Instead of writing separate try-catch blocks for each error, ?= lets you handle errors directly in one line. This keeps your code cleaner and easier to read.

#### Here’s how the ?= operator works:

- It returns a pair of values: [error, result].
- If an error happens, the first value is the error, and the second is null.
- If there’s no error, the first value is null, and the second value is the result.

Let’s see how it simplifies our earlier example:
```
const [error, data] = await fetch("https://api.example.com/data").json()

if (error) {
    console.error('Error occurred:', error);
} else {
    console.log('Data fetched successfully:', data);
}

```
In this version, both network errors and JSON parsing errors are handled in a single line. There’s no need for nested try-catch blocks, making the code cleaner and more direct.

#### Old Way (with try-catch):
```
async function loadConfig() {
    try {
        const fileContents = await readFile("config.json");
        try {
            const config = JSON.parse(fileContents);
            return config;
        } catch (parseError) {
            console.error('Error parsing JSON:', parseError);
        }
    } catch (readError) {
        console.error('Error reading file:', readError);
    }
}
```
#### New Way (with ?=):
```
const [readError, fileContents] = await readFile("config.json")
    .then(data => [null, data])
    .catch(err => [err, null]);

if (readError) {
    console.error('Error reading file:', readError);
} else {
    let config;
    try {
        config = JSON.parse(fileContents);
        console.log('Configuration loaded successfully:', config);
    } catch (parseError) {
        console.error('Error parsing JSON:', parseError);
    }
}
```
See how much simpler the second version is? It’s easy to read and removes redundant code.

Looking Ahead: The Future of Error Handling in JavaScript
The ?= operator isn’t just a minor change—it represents a new, simplified approach to error handling in JavaScript. As JavaScript continues to evolve, tools like this help make it a more powerful, modern language for building web and server applications.
---

