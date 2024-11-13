## 5. Loops

Loops are used to repeat code.

#### The For Loop

The for statement creates a loop with 3 optional expressions:

```javascript
for (expression 1; expression 2; expression 3) { // code block to be executed
}
```

**Expression 1** is executed (one time) before the execution of the code block.
**Expression 2** defines the condition for executing the code block.
**Expression 3** is executed (every time) after the code block has been executed.

```javascript
let arr = [1, 2, 3, 4, 5];
for (let i = 0; i < arr.length; i++) {
  console.log(arr[i]);
}
```

##### For of

```javascript
let item = [10, 20, 30, 40];
let i = 0;
for (let val of item) {
  console.log(`value at index ${i}=${val}`);
  let offer = val / 10;
  item[i] = item[i] - offer;
  console.log(`after offer ${item[i]}`);
  i++;
}
```

```javascript
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

```javascript
const person = { fname: "John", lname: "Doe", age: 25 };

let text = "";
for (let x in person) {
  text += person[x]; //John Doe 25
}
```

#### while loop:

- **The while loop loops through a block of code as long as a specified condition is true.**

```javascript
while (condition) {
  // code block to be executed
}
```

```javascript
let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

---
