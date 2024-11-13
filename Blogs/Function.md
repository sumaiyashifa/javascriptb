## 4. Functions

A JavaScript function is a block of code designed to perform a particular task.It is executed when "something" invokes it (calls it).

```javascript
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

```javascript
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

```javascript
function countvowel(str) {
  let c = 0;
  for (const char of str) {
    if (
      char == "a" ||
      char == "e" ||
      char == "i" ||
      char == "o" ||
      char == "u"
    ) {
      c++;
    }
  }
  console.log(c);
}
countvowel("i am a girl");
```

- **Arrow Function**:

```javascript
const arrowmul = (a, b) => {
  return a * b;
};
```

- **Bind Function**:

```javascript
let obj = { x: 5 };
function getX() {
  return this.x;
}
let boundGetX = getX.bind(obj);
```

---
