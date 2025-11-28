# 🔁 Higher-Order Functions in JavaScript

Higher-order functions are functions that can **take other functions as arguments**, **return functions**, or **do both**.  
They are a fundamental part of modern JavaScript and enable cleaner, more powerful, and more expressive code.

---

## ✅ What Is a Higher-Order Function?

A **Higher-Order Function (HOF)** is any function that:

- Accepts a function as a parameter  
**or**
- Returns a function  

Example:

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

function processUser(callback, userName) {
  return callback(userName);
}

console.log(processUser(greet, "Abideen"));
// Output: Hello, Abideen!
````

---

# 1️⃣ Functions as Arguments

JavaScript allows you to pass functions just like values.

### Example: Passing a function to another function

```javascript
function add(a, b) {
  return a + b;
}

function calculate(operation, x, y) {
  return operation(x, y);
}

console.log(calculate(add, 5, 3));  
// Output: 8
```

---

# 2️⃣ Functions Returning Functions

A function can also **return another function**.

### Example:

```javascript
function multiplier(factor) {
  return function (number) {
    return number * factor;
  };
}

const double = multiplier(2);
console.log(double(10));  
// Output: 20
```

---

# 3️⃣ Common Higher-Order Functions in JavaScript

JavaScript arrays come with built-in higher-order functions:

---

## 📌 `map()`

Transforms each element in an array and returns a **new array**.

```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(n => n * 2);

console.log(doubled);  
// Output: [2, 4, 6]
```

---

## 📌 `filter()`

Keeps elements that pass a condition.

```javascript
const ages = [12, 17, 20, 25];
const adults = ages.filter(age => age >= 18);

console.log(adults);  
// Output: [20, 25]
```

---

## 📌 `reduce()`

Reduces an array to a single value.

```javascript
const nums = [1, 2, 3, 4];
const sum = nums.reduce((total, n) => total + n, 0);

console.log(sum);  
// Output: 10
```

---

# 4️⃣ Why Use Higher-Order Functions?

* Cleaner, more readable code
* Reduces repetition
* Makes code more modular
* Enables functional programming patterns
* Helps handle async code and callbacks

---

# 5️⃣ Real-Life Examples

### 🔹 Running multiple actions on a button click

```javascript
function logClick() { console.log("Clicked!"); }
function changeColor() { document.body.style.background = "yellow"; }

function handleEvent(...callbacks) {
  return () => callbacks.forEach(fn => fn());
}

document.querySelector("button")
  .addEventListener("click", handleEvent(logClick, changeColor));
```

---

# 🧪 Practice Exercises

### ✏️ Exercise 1

Write a function `applyTwice` that takes a function and a value and applies the function two times.

Example:

```javascript
applyTwice(x => x + 1, 5); // 7
```

---

### ✏️ Exercise 2

Use `filter()` to return only even numbers from an array.

---

### ✏️ Exercise 3

Use `map()` to convert an array of names to uppercase.

---

### ✏️ Exercise 4

Use `reduce()` to find the maximum value in an array.

---

# 🎯 Summary

Higher-order functions:

* Accept functions as arguments
* Return functions
* Enable powerful built-in methods like `map`, `filter`, and `reduce`
* Make JavaScript more expressive and reusable

They are a crucial part of modern JavaScript development.

