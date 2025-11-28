# 📦 JavaScript Modules

Modules allow you to **split your code into separate files** and **reuse functionality** across your application.  
This makes your code **organized, maintainable, and scalable**.

---

## 1️⃣ Exporting from a Module

You can export variables, functions, or classes from a file.

```javascript
// math.js
export const add = (a, b) => a + b;
export const subtract = (a, b) => a - b;

// Default export
export default function multiply(a, b) {
  return a * b;
}
````

* `export` → named export (can export multiple items)
* `export default` → default export (one per file)

---

## 2️⃣ Importing Modules

### Named Imports

```javascript
// main.js
import { add, subtract } from './math.js';

console.log(add(5, 3));       // 8
console.log(subtract(5, 3));  // 2
```

### Default Import

```javascript
import multiply from './math.js';

console.log(multiply(5, 3)); // 15
```

### Rename Imports

```javascript
import { add as sum } from './math.js';
console.log(sum(2, 3)); // 5
```

---

## 3️⃣ Combining Named and Default Exports

```javascript
// math.js
export const divide = (a, b) => a / b;
export default function multiply(a, b) {
  return a * b;
}

// main.js
import multiply, { divide } from './math.js';
console.log(multiply(4, 5)); // 20
console.log(divide(10, 2));  // 5
```

---

## 4️⃣ Importing All

```javascript
import * as MathFunctions from './math.js';

console.log(MathFunctions.divide(9, 3));       // 3
console.log(MathFunctions.default(4, 5));     // 20
```

* `* as name` imports all exports as an object

---

## 5️⃣ Practical Applications

* Split code into **reusable modules** for large projects
* Keep **utility functions** in separate files
* Organize **components, services, or API calls** in modular structure
* Combine multiple modules for **clean architecture**

---

## 📝 Exercises

1. Create a module `greetings.js` that exports two functions: `sayHello` and `sayGoodbye`.
2. Import `sayHello` in `main.js` and call it.
3. Create a default export function in a module and import it.
4. Rename an import using `as`.
5. Use `import * as` to import all functions from a module and call them.

---

# 🎯 Summary

* **Modules** allow splitting code into separate files for clarity and reuse.
* Use `export` for named exports and `export default` for default exports.
* Import using `import { name } from './file.js'` or `import name from './file.js'`.
* Use modules to **organize utilities, components, and logic** in real projects.

Do you want me to do that next?
```
