# 🔧 Functions in JavaScript

Functions are **reusable blocks of code** that perform a specific task.
They help you avoid repetition and make your code organized, readable, and modular.

---

## ✅ Why Use Functions?

* Reuse code without rewriting it
* Organize logic into small pieces
* Make code easier to maintain
* Improve readability

---

# 🧱 1. Function Declaration

This is the standard way to define a function.

```js
function greet() {
  console.log("Hello, world!");
}

greet(); // Output: Hello, world!
```

---

# 🧱 2. Function with Parameters

Parameters allow you to pass values into a function.

```js
function sayHello(name) {
  console.log("Hello, " + name);
}

sayHello("Ayo"); // Output: Hello, Ayo
```

---

# 🧱 3. Function with Return Value

`return` sends data back from the function.

```js
function add(a, b) {
  return a + b;
}

const result = add(5, 3);
console.log(result); // Output: 8
```

---

# 🧱 4. Function Expression

Functions can be stored in variables.

```js
const multiply = function (x, y) {
  return x * y;
};

console.log(multiply(4, 2)); // Output: 8
```

---

# 🧱 5. Arrow Functions (ES6)

Shorter syntax introduced in ES6.

```js
const square = (n) => {
  return n * n;
};

console.log(square(6)); // Output: 36
```

**One-line return:**

```js
const double = n => n * 2;
```

---

# 🧱 6. Default Parameters

Used when a value is not provided.

```js
function greet(name = "Guest") {
  console.log("Welcome, " + name);
}

greet();          // Output: Welcome, Guest
greet("Tunde");   // Output: Welcome, Tunde
```

---

# 🧱 7. Rest Parameters (`...rest`)

Collects multiple arguments into an array.

```js
function sum(...numbers) {
  return numbers.reduce((total, n) => total + n, 0);
}

console.log(sum(1, 2, 3, 4)); // Output: 10
```

---

# 🧱 8. Callback Functions

Functions can be passed into other functions.

```js
function display(result) {
  console.log("Result:", result);
}

function calculate(a, b, callback) {
  callback(a + b);
}

calculate(5, 3, display); // Output: Result: 8
```

---

# 🧱 9. Function Scope

Variables inside a function are not accessible outside it.

```js
function test() {
  let x = 10;
  console.log(x); // 10
}

test();
// console.log(x); // Error: x is not defined
```

---

# 🧪 Practice Exercises

Try these:

1. Create a function that returns the area of a rectangle.
2. Write a function that checks if a number is even or odd.
3. Create an arrow function that multiplies two numbers.
4. Write a function that takes an array and returns the largest number.
5. Create a function that takes a name and returns `"Hello, <name>"`.
