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

```javascript
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
      console.error("Failed to parse JSON:", error);
    } else {
      console.error("Network request failed:", error);
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

```javascript
const [error, data] = await fetch("https://api.example.com/data").json();

if (error) {
  console.error("Error occurred:", error);
} else {
  console.log("Data fetched successfully:", data);
}
```

In this version, both network errors and JSON parsing errors are handled in a single line. There’s no need for nested try-catch blocks, making the code cleaner and more direct.

#### Old Way (with try-catch):

```javascript
async function loadConfig() {
  try {
    const fileContents = await readFile("config.json");
    try {
      const config = JSON.parse(fileContents);
      return config;
    } catch (parseError) {
      console.error("Error parsing JSON:", parseError);
    }
  } catch (readError) {
    console.error("Error reading file:", readError);
  }
}
```

#### New Way (with ?=):

```javascript
const [readError, fileContents] = await readFile("config.json")
  .then((data) => [null, data])
  .catch((err) => [err, null]);

if (readError) {
  console.error("Error reading file:", readError);
} else {
  let config;
  try {
    config = JSON.parse(fileContents);
    console.log("Configuration loaded successfully:", config);
  } catch (parseError) {
    console.error("Error parsing JSON:", parseError);
  }
}
```

See how much simpler the second version is? It’s easy to read and removes redundant code.

Looking Ahead: The Future of Error Handling in JavaScript
The ?= operator isn’t just a minor change—it represents a new, simplified approach to error handling in JavaScript. As JavaScript continues to evolve, tools like this help make it a more powerful, modern language for building web and server applications.

---
