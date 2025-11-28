# 🐞 Debugging Techniques in JavaScript

Debugging is the process of **finding and fixing errors** in your code.  
It is a **foundation for writing reliable and maintainable code**.

---

## 1️⃣ Using `console.log()`

The simplest way to debug is by **logging values** to the console.

```javascript
let x = 10;
let y = 0;

console.log("x:", x, "y:", y);

let result = x / y;
console.log("Result:", result);
````

* Helps inspect **variables, object values, and function outputs**.

---

## 2️⃣ Browser Developer Tools

Every modern browser has **built-in developer tools**:

* Open DevTools: `F12` or `Ctrl+Shift+I` / `Cmd+Option+I`
* **Console Tab** → View logs, errors, and warnings
* **Elements Tab** → Inspect and edit HTML/CSS live
* **Sources Tab** → View JS files and set breakpoints

---

## 3️⃣ Breakpoints

Breakpoints pause code execution at a specific line so you can **inspect variables and program flow**.

1. Open DevTools → Sources Tab
2. Click the line number in your JS file to set a breakpoint
3. Reload the page → code pauses at breakpoint
4. Step through code:

   * Step Over → next line
   * Step Into → inside function
   * Step Out → exit function

---

## 4️⃣ Inspecting Network Requests

* **Network Tab** → see API calls, status codes, request/response data
* Useful for debugging **Fetch API, AJAX, or external resources**

```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then(res => res.json())
  .then(data => console.log(data))
  .catch(err => console.error(err));
```

* Inspect request → check **URL, method, headers, response**

---

## 📝 Tips for Effective Debugging

* Use `console.log()` to trace values and execution order
* Check **error messages** in the console carefully
* Use **breakpoints** for complex logic
* Test **small sections of code** instead of everything at once
* Inspect network requests when fetching data from APIs

---

# 🎯 Summary

* Debugging is essential to write **reliable and maintainable JavaScript**.
* Tools: `console.log`, breakpoints, browser DevTools, Network inspection
* Combines **inspection, testing, and iterative fixes** to resolve errors efficiently.


Do you want me to continue with **Form Handling & Validation** next?
```
