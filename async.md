# ⏱️ Asynchronous JavaScript

JavaScript is **single-threaded**, meaning it executes code **one line at a time**.  
Asynchronous JavaScript allows your code to **perform tasks in the background** (like fetching data) without blocking the main thread.

---

## 1️⃣ Callbacks

A **callback** is a function passed into another function to be executed later.

```javascript
function fetchData(callback) {
  setTimeout(() => {
    callback("Data received");
  }, 2000);
}

fetchData((result) => {
  console.log(result); // "Data received" after 2 seconds
});
````

> Problem: callbacks can become **nested and hard to read** ("callback hell").

---

## 2️⃣ Promises

A **Promise** represents a value that may be available **now, later, or never**.

```javascript
const fetchData = new Promise((resolve, reject) => {
  const success = true;
  if (success) {
    resolve("Data received");
  } else {
    reject("Error occurred");
  }
});

fetchData
  .then(response => console.log(response))
  .catch(error => console.log(error));
```

* `resolve` → when operation succeeds
* `reject` → when operation fails
* `then` → handles success
* `catch` → handles error

---

## 3️⃣ Async/Await

`async` and `await` allow you to write asynchronous code **like synchronous code**.

```javascript
function getData() {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve("Data received");
    }, 2000);
  });
}

async function fetchData() {
  const result = await getData();
  console.log(result);
}

fetchData(); // prints "Data received" after 2 seconds
```

* `async` → marks a function as asynchronous
* `await` → waits for a promise to resolve

---

## 4️⃣ Fetch API

The **Fetch API** is used to request data from a server.

```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error(error));
```

**With async/await:**

```javascript
async function getPost() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts/1");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

getPost();
```

---

## 5️⃣ Practical Applications

* Load data from APIs without blocking the page
* Perform animations while fetching resources
* Handle multiple asynchronous requests simultaneously
* Build interactive, responsive web apps

---

## 📝 Exercises

1. Create a Promise that resolves after 3 seconds and logs a message.
2. Rewrite a Promise using `async/await`.
3. Fetch data from `https://jsonplaceholder.typicode.com/users` and log it to the console.
4. Handle errors using `.catch()` or `try/catch`.
5. Simulate a network request with `setTimeout` and use a callback to log the result.

---

# 🎯 Summary

* **Callbacks, Promises, and async/await** handle asynchronous code.
* **Promises** prevent callback hell.
* **async/await** makes asynchronous code readable like synchronous code.
* **Fetch API** is used for server requests.
* Asynchronous JavaScript is essential for **interactive, responsive applications**.

