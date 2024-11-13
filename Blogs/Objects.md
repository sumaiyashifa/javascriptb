## 6. Objects

You have already learned that JavaScript variables are containers for data values.Objects are variables too. But objects can contain many values. This code assigns many values (Fiat, 500, white) to a variable named car:The values are written as name:value pairs (name and value separated by a colon).

```javascript
const car = { type: "Fiat", model: "500", color: "white" };
```

#### Creating an Object

```javascript
const student = {
  name: "shifa",
  ispresent: true,
};
let output = `My name is ${student.name} \npresent is ${student.ispresent}`;
console.log(output);

// My name is shifa
// present is true
```

Objects can also have methods.Methods are actions that can be performed on objects.Methods are stored in properties as function definitions.A method is a function stored as a property.

#### Creating an Object with Method

```javascript
const person = {
  firstName: "John",
  lastName: "Doe",
  id: 5566,
  fullName: function () {
    return this.firstName + " " + this.lastName;
  },
};
```

#### Accessing Object Methods

objectName.methodName()

- name = person.fullName();

---
