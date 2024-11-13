## 3. Data Types

JavaScript variables can hold numbers like 100 and text values like "John Doe".In programming, text values are called text strings.JavaScript can handle many types of data, but for now, just think of numbers and strings. Strings are written inside double or single quotes. Numbers are written without quotes.If you put a number in quotes, it will be treated as a text string.

JavaScript has the following data types:

- **Primitive**: `String`, `Number`, `BigInt`, `Boolean`, `Undefined`, `Null`, `Symbol`
- **Complex**: `Object` (e.g., arrays, functions, maps, sets)

```javascript
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
const person = { firstName: "John", lastName: "Doe" };

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");

//Symbol :
let symbol1 = Symbol("Khan");
let symbol2 = Symbol("Khan");

// Each time Symbol() method  is used to create new global Symbol
console.log(symbol1 == symbol2); // False (because symbols are always unique)
```

When adding a number and a string, JavaScript will treat the number as a string.

```javascript
let x = "5" + "world";
```

---
