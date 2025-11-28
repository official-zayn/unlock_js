# ⏳ Promises in Depth & Async Patterns

Promises are a core part of JavaScript’s **asynchronous programming**, allowing you to handle tasks that take time to complete (like API requests, timers, or file operations).

---

## 1️⃣ What is a Promise?

A **Promise** represents a value that may be available **now, in the future, or never**.

```javascript
const myPromise = new Promise((resolve, reject) => {
  const success = true;

  setTimeout(() => {
    if (success) {
      resolve("Task completed successfully!");
    } else {
      reject("Task failed!");
    }
  }, 1000);
});

myPromise
  .then(result => console.log(result))
  .catch(error => console.error(error));
````

* `resolve(value)` → Promise fulfilled
* `reject(error)` → Promise rejected
* `.then()` → handle success
* `.catch()` → handle errors

---

## 2️⃣ Chaining Promises

```javascript
const multiplyBy2 = num => Promise.resolve(num * 2);

multiplyBy2(5)
  .then(result => result + 3)
  .then(final => console.log(final)) // 13
  .catch(err => console.error(err));
```

* Promises can be **chained** for sequential async operations

---

## 3️⃣ Parallel Execution with `Promise.all`

```javascript
const p1 = Promise.resolve(10);
const p2 = Promise.resolve(20);
const p3 = Promise.resolve(30);

Promise.all([p1, p2, p3])
  .then(results => console.log(results)) // [10, 20, 30]
  .catch(err => console.error(err));
```

* Waits for **all promises** to resolve
* If **any promise rejects**, the whole chain rejects

---

## 4️⃣ `Promise.race` – First Promise Wins

```javascript
const p1 = new Promise(res => setTimeout(() => res("First"), 1000));
const p2 = new Promise(res => setTimeout(() => res("Second"), 2000));

Promise.race([p1, p2]).then(result => console.log(result)); // "First"
```

* Resolves or rejects **as soon as one promise settles**

---

## 5️⃣ Converting Callbacks to Promises

```javascript
function delay(ms) {
  return new Promise(resolve => setTimeout(resolve, ms));
}

delay(2000).then(() => console.log("Executed after 2 seconds"));
```

* Makes **callback-based code cleaner and more readable**

---

## 6️⃣ Async/Await Pattern

```javascript
function fetchData() {
  return new Promise(res => setTimeout(() => res("Data received"), 1500));
}

async function getData() {
  try {
    const data = await fetchData();
    console.log(data);
  } catch (err) {
    console.error(err);
  }
}

getData();
```

* `async` function → returns a promise
* `await` → pause execution until the promise resolves
* Makes async code **look synchronous**

---

## 📝 Exercises

1. Create a promise that resolves after 3 seconds and logs a message.
2. Chain 3 promises to perform sequential arithmetic operations.
3. Use `Promise.all` to fetch 3 different URLs and log the results.
4. Implement `Promise.race` with 2 timeouts to see which resolves first.
5. Rewrite a callback-based function (like `setTimeout`) using promises and async/await.

---

# 🎯 Summary

* Promises provide a **structured way to handle async operations**.
* Use `.then()/.catch()` for chaining, `Promise.all` for parallel tasks, and `Promise.race` for fastest response.
* **Async/await** makes code cleaner and easier to read.
* Promises are **essential for APIs, timers, and any asynchronous logic** in web development.

