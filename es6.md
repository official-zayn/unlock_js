# 🚀 ES6 Features in JavaScript

ES6 (ECMAScript 2015) introduced **modern syntax and features** that make JavaScript easier to write, read, and maintain.  
Here are the most commonly used ES6 features.

---

## 1️⃣ `let` and `const`

- `let` → block-scoped variable  
- `const` → block-scoped constant (cannot be reassigned)

```javascript
let name = "Abideen";
name = "Tunde"; // ✅ allowed

const pi = 3.14;
pi = 3.1415;    // ❌ Error: cannot reassign
````

> Avoid `var`; use `let` and `const` for clarity and safety.

---

## 2️⃣ Template Literals

* Use backticks `` ` `` to create strings
* Can embed expressions using `${}`

```javascript
let name = "Abideen";
let age = 25;
console.log(`My name is ${name} and I am ${age} years old.`);
```

---

## 3️⃣ Arrow Functions

* Shorter syntax for functions
* `this` is lexically scoped

```javascript
// Traditional function
function sum(a, b) {
  return a + b;
}

// Arrow function
const sumArrow = (a, b) => a + b;

console.log(sumArrow(5, 3)); // 8
```

---

## 4️⃣ Default Parameters

```javascript
function greet(name = "Guest") {
  console.log(`Hello, ${name}!`);
}

greet("Tunde"); // Hello, Tunde!
greet();        // Hello, Guest!
```

---

## 5️⃣ Destructuring

### Objects

```javascript
const person = { name: "Abideen", age: 25 };
const { name, age } = person;
console.log(name, age); // Abideen 25
```

### Arrays

```javascript
const numbers = [1, 2, 3];
const [first, second] = numbers;
console.log(first, second); // 1 2
```

---

## 6️⃣ Spread & Rest Operators

### Spread → expand array or object

```javascript
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4];
console.log(arr2); // [1, 2, 3, 4]
```

### Rest → gather remaining elements

```javascript
function sum(...numbers) {
  return numbers.reduce((a, b) => a + b, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
```

---

## 7️⃣ `for...of` Loop

Iterate over iterable objects (arrays, strings)

```javascript
const fruits = ["apple", "banana", "orange"];
for (const fruit of fruits) {
  console.log(fruit);
}
```

---

## 8️⃣ `Map` and `Set`

### Map → key-value pairs

```javascript
const map = new Map();
map.set("name", "Abideen");
map.set("age", 25);
console.log(map.get("name")); // Abideen
```

### Set → unique values

```javascript
const set = new Set([1, 2, 2, 3]);
console.log(set); // {1, 2, 3}
```

---

## 9️⃣ Modules (ES6 Modules)

* Export and import code between files

```javascript
// math.js
export const add = (a, b) => a + b;

// main.js
import { add } from './math.js';
console.log(add(5, 3)); // 8
```

---

## 10️⃣ Promises

* Handle asynchronous operations more cleanly

```javascript
const fetchData = new Promise((resolve, reject) => {
  let success = true;
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

---

## 📝 Exercises

1. Rewrite a traditional function as an arrow function.
2. Use template literals to display a sentence with variables.
3. Destructure an object and an array into separate variables.
4. Combine two arrays using the spread operator.
5. Create a Set with duplicate values and print the unique values.
6. Create a Map with at least two key-value pairs and retrieve a value.
7. Write a simple Promise that resolves or rejects based on a condition.

---

# 🎯 Summary

* ES6 introduces **let, const, template literals, arrow functions, destructuring, spread/rest, for...of, Map/Set, modules, and Promises**.
* Makes code **cleaner, safer, and easier to read**.
* Essential for **modern JavaScript development**.


