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

```javascript
const pi = 3.14159265359;
```

---
