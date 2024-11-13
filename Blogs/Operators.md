## 2. Operators

JavaScript uses different operators to perform calculations, comparisons, and other operations.

### Arithmetic Operators

```javascript
let x = 5;
let y = 2;
let z = x % y; //  1
```

### Assignment Operators

| Operator | Description                                    | Example                          | Equivalent Expression |
| -------- | ---------------------------------------------- | -------------------------------- | --------------------- | ------------------ | --- | ------ | --- |
| `=`      | Assigns right-hand value to left-hand variable | `x = 5`                          | `x = 5`               |
| `+=`     | Adds and assigns                               | `x += 2` (same as `x = x + 2`)   | `x = x + 2`           |
| `-=`     | Subtracts and assigns                          | `x -= 2` (same as `x = x - 2`)   | `x = x - 2`           |
| `*=`     | Multiplies and assigns                         | `x *= 2` (same as `x = x * 2`)   | `x = x * 2`           |
| `/=`     | Divides and assigns                            | `x /= 2` (same as `x = x / 2`)   | `x = x / 2`           |
| `%=`     | Modulus and assigns                            | `x %= 2` (same as `x = x % 2`)   | `x = x % 2`           |
| `**=`    | Exponentiation and assigns                     | `x **= 2` (same as `x = x ** 2`) | `x = x ** 2`          |
| `<<=`    | Left shift and assigns                         | `x <<= 2` (same as `x = x << 2`) | `x = x << 2`          |
| `>>=`    | Right shift and assigns                        | `x >>= 2` (same as `x = x >> 2`) | `x = x >> 2`          |
| `&=`     | Bitwise AND and assigns                        | `x &= 2` (same as `x = x & 2`)   | `x = x & 2`           |
| `        | =`                                             | Bitwise OR and assigns           | `x                    | = 2`(same as`x = x | 2`) | `x = x | 2`  |
| `^=`     | Bitwise XOR and assigns                        | `x ^= 2` (same as `x = x ^ 2`)   | `x = x ^ 2`           |

- JavaScript uses an assignment operator ( = ) to assign values to variables:

```javascript
let text = "Hello";
text += " World"; // Hello World
```

### Simple Assignment and Chaining:

```javascript
let x = 5;
let y = 10;
let z = 25;

x = y; // x is 10
x = y = z; // x, y and z are all 25
```

The assignment expression itself evaluates to the value of the right-hand side, so you can log the value and assign to a variable at the same time.

```javascript
let x;
console.log(x); // undefined
console.log((x = 2)); // 2
console.log(x); // 2
```

### JavaScript Comparison Operators

| Operator | Name                  | Description                                                     | Example               |
| -------- | --------------------- | --------------------------------------------------------------- | --------------------- |
| `==`     | Equality              | Checks if values are equal after type coercion.                 | `5 == "5"` → `true`   |
| `===`    | Strict Equality       | Checks if values and types are equal without type coercion.     | `5 === "5"` → `false` |
| `!=`     | Inequality            | Checks if values are not equal after type coercion.             | `5 != "5"` → `false`  |
| `!==`    | Strict Inequality     | Checks if values and types are not equal without type coercion. | `5 !== "5"` → `true`  |
| `>`      | Greater Than          | Checks if the left value is greater than the right.             | `5 > 3` → `true`      |
| `<`      | Less Than             | Checks if the left value is less than the right.                | `5 < 3` → `false`     |
| `>=`     | Greater Than or Equal | Checks if the left value is greater than or equal to the right. | `5 >= 5` → `true`     |
| `<=`     | Less Than or Equal    | Checks if the left value is less than or equal to the right.    | `5 <= 3` → `false`    |

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

| Operator | Name                  | Description                                                                                        | Example                                                                                   |
| -------- | --------------------- | -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- | --- | ------ |
| `&`      | AND                   | Performs a bitwise AND operation; sets each bit to `1` if both bits are `1`.                       | `5 & 3` → `1`                                                                             |
| `        | `                     | OR                                                                                                 | Performs a bitwise OR operation; sets each bit to `1` if at least one of the bits is `1`. | `5  | 3`→`7` |
| `^`      | XOR                   | Performs a bitwise XOR operation; sets each bit to `1` only if one of the bits is `1`, not both.   | `5 ^ 3` → `6`                                                                             |
| `~`      | NOT                   | Inverts all bits; flips each bit, turning `1`s to `0`s and `0`s to `1`s.                           | `~5` → `-6`                                                                               |
| `<<`     | Left Shift            | Shifts bits to the left by specified number of positions, adding `0`s on the right.                | `5 << 1` → `10`                                                                           |
| `>>`     | Right Shift           | Shifts bits to the right by specified number of positions, preserving the sign bit (signed shift). | `5 >> 1` → `2`                                                                            |
| `>>>`    | Zero-fill Right Shift | Shifts bits to the right by specified positions, filling the left with `0`s (unsigned shift).      | `5 >>> 1` → `2`                                                                           |

Example of signed and unsigned right shifts:

```javascript
let x = -8;
console.log(x >> 2); // -2 (Signed right shift)
console.log(x >>> 2); // 1073741822 (Unsigned right shift)
```

> > (Signed Right Shift):
> > The >> operator shifts the bits of a number to the right. It preserves the sign bit, which means that if the number is positive, it pads the left side with zeros, and if the number is negative, it pads the left side with ones.
> > Example: x >> y shifts the bits of x to the right by y positions.
> >
> > > (Unsigned Right Shift):
> > > The >>> operator also shifts the bits to the right, but it always pads the left side with zeros, regardless of the sign of the number. It treats the number as if it were an unsigned integer.
> > > Example: x >>> y shifts the bits of x to the right by y positions, and the left side is always padded with zeros.
> > > Here's a quick example to illustrate the difference:
> > > Bitwise XOR:

The bitwise XOR (^) operator returns a number or BigInt whose binary representation has a 1 in each bit position for which the corresponding bits of either but not both operands are 1.

```javascript
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

```javascript
let greeting = "Hello, " + "world!"; //  "Hello, world!"
```

##### 2. Concatenation Assignment (+= Operator)

The += operator appends one string to another and assigns the result to the original variable.

```javascript
let message = "Hello";
message += ", world!"; // message becomes "Hello, world!"
```

### `typeof` Operator in JavaScript

The `typeof` operator is used to check the data type of a variable or value in JavaScript.
A complex data type can store multiple values and/or different data types together.
JavaScript has one complex data type:

- object

All other complex types like arrays, functions, sets, and maps are just different types of objects.

| Value               | Expression                 | Output        | Description                          |
| ------------------- | -------------------------- | ------------- | ------------------------------------ |
| `"Hello"`           | `typeof "Hello"`           | `"string"`    | String data type                     |
| `42`                | `typeof 42`                | `"number"`    | Number data type                     |
| `true`              | `typeof true`              | `"boolean"`   | Boolean data type                    |
| `undefined`         | `typeof undefined`         | `"undefined"` | Undefined data type                  |
| `Symbol("id")`      | `typeof Symbol("id")`      | `"symbol"`    | Symbol data type                     |
| `9007199254740991n` | `typeof 9007199254740991n` | `"bigint"`    | BigInt data type                     |
| `null`              | `typeof null`              | `"object"`    | Null (historically returns "object") |
| `{ name: 'John' }`  | `typeof { name: 'John' }`  | `"object"`    | Object data type                     |
| `[1, 2, 3, 4]`      | `typeof [1, 2, 3, 4]`      | `"object"`    | Array (treated as object)            |
| `new Map()`         | `typeof new Map()`         | `"object"`    | Map (treated as object)              |
| `new Set()`         | `typeof new Set()`         | `"object"`    | Set (treated as object)              |
| `function() {}`     | `typeof function() {}`     | `"function"`  | Function data type                   |

### The instanceof Operator

The instanceof operator returns true if an object is an instance of a specified object type:

```javascript
const time = new Date();

time instanceof Date; //Date:True
```

```javascript
const myArray = [1, 2, 3];
console.log(myArray instanceof Array); // true
console.log(myArray instanceof Object); //  true
console.log(myArray instanceof Date); //  false
```

---
