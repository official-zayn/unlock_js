# ⚠️ JavaScript Error Handling

Errors happen when something goes wrong in your code.  
JavaScript provides ways to **catch and handle errors gracefully** so your program doesn’t crash.

---

## 1️⃣ Common Types of Errors

| Type              | Description                                     | Example                          |
|------------------|-------------------------------------------------|----------------------------------|
| SyntaxError       | Mistake in code syntax                          | `let x = ;`                      |
| ReferenceError    | Variable not defined                             | `console.log(a);`                |
| TypeError         | Wrong data type or operation                     | `"hello".push("!");`             |
| RangeError        | Number out of range                               | `(123).toPrecision(500);`        |
| EvalError         | Error in `eval()` function                        | `eval("x ===");`                  |

---

## 2️⃣ Try…Catch

```javascript
try {
  let result = riskyOperation();
  console.log(result);
} catch (error) {
  console.error("An error occurred:", error.message);
}
````

* `try` → code that might fail
* `catch` → code to run if an error occurs
* `error.message` → shows the error message

---

## 3️⃣ Finally

```javascript
try {
  let data = fetchData();
} catch (error) {
  console.error(error);
} finally {
  console.log("This always runs, success or failure.");
}
```

* `finally` runs **regardless of success or failure**
* Useful for **cleanup tasks** (closing files, stopping loaders, etc.)

---

## 4️⃣ Throwing Custom Errors

```javascript
function checkAge(age) {
  if (age < 18) {
    throw new Error("You must be at least 18 years old.");
  }
  return "Access granted";
}

try {
  console.log(checkAge(15));
} catch (error) {
  console.error(error.message); // "You must be at least 18 years old."
}
```

* `throw` allows you to **create custom errors**
* Combine with `try…catch` for control flow

---

## 5️⃣ Error Handling with Async/Await

```javascript
async function fetchData() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts/1");
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Fetch error:", error.message);
  }
}
fetchData();
```

* Always check `response.ok` for HTTP errors
* Use `try…catch` to handle asynchronous errors

---

## 📝 Exercises

1. Create a function that throws an error if a number is negative.
2. Use try…catch to handle a function that may throw an error.
3. Write a `finally` block that logs a message regardless of success or failure.
4. Fetch data from an API and handle network errors using `try…catch`.
5. Create a custom error message for invalid user input.

---

# 🎯 Summary

* JavaScript errors can be **caught and handled** to prevent crashes.
* Use **try…catch…finally** for synchronous code.
* Use **throw** for custom errors.
* Always handle errors in asynchronous code with **try…catch** or `.catch()`.
* Proper error handling improves **robustness and user experience**.

