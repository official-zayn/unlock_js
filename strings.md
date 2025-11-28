# 🔤 Strings & Numbers in JavaScript

Strings and numbers are **fundamental data types** in JavaScript.  
- **Strings** → text, e.g., `"Hello World"`  
- **Numbers** → numeric values, e.g., `42` or `3.14`  

---

## 1️⃣ Strings

### Creating Strings
```javascript
let name = "Abideen";
let greeting = 'Hello';
let message = `Hi, ${name}!`; // Template literals
````

### Common String Operations

| Operation     | Example                                           | Output            |
| ------------- | ------------------------------------------------- | ----------------- |
| Concatenation | `"Hello " + "World"`                              | "Hello World"     |
| Length        | `"Hello".length`                                  | 5                 |
| Access char   | `"Hello"[1]`                                      | "e"               |
| Slice         | `"Hello".slice(1,4)`                              | "ell"             |
| Replace       | `"Hello".replace("H","J")`                        | "Jello"           |
| Upper / Lower | `"Hello".toUpperCase()` / `"Hello".toLowerCase()` | "HELLO" / "hello" |

### Example

```javascript
let str = "JavaScript";
console.log(str.length);          // 10
console.log(str[0]);              // "J"
console.log(str.slice(0,4));      // "Java"
console.log(`Welcome, ${str}!`);  // "Welcome, JavaScript!"
```

---

## 2️⃣ Numbers

### Creating Numbers

```javascript
let age = 25;
let pi = 3.14159;
```

### Common Number Operations

| Operation      | Example  | Output |
| -------------- | -------- | ------ |
| Addition       | `5 + 2`  | 7      |
| Subtraction    | `5 - 2`  | 3      |
| Multiplication | `5 * 2`  | 10     |
| Division       | `10 / 2` | 5      |
| Modulus        | `10 % 3` | 1      |
| Exponent       | `2 ** 3` | 8      |

### Number Methods

```javascript
let num = 3.456;
console.log(num.toFixed(2));  // "3.46"
console.log(Number("42"));    // 42
console.log(parseInt("42px"));// 42
console.log(parseFloat("3.14"));// 3.14
```

---

## 3️⃣ Combining Strings and Numbers

```javascript
let name = "Abideen";
let age = 25;

console.log(name + " is " + age + " years old."); // Concatenation
console.log(`${name} is ${age} years old.`);     // Template literal
```

---

## 4️⃣ Useful String Methods

| Method         | Description                   |
| -------------- | ----------------------------- |
| `trim()`       | Removes spaces at start/end   |
| `includes()`   | Checks if substring exists    |
| `startsWith()` | Checks start of string        |
| `endsWith()`   | Checks end of string          |
| `split()`      | Converts string to array      |
| `repeat()`     | Repeats string multiple times |

```javascript
let text = "  Hello World  ";
console.log(text.trim());        // "Hello World"
console.log(text.includes("World")); // true
console.log(text.split(" "));    // ["", "", "Hello", "World", "", ""]
console.log("Hi! ".repeat(3));   // "Hi! Hi! Hi! "
```

---

## 5️⃣ Useful Number Methods

| Method/Property | Description                          |
| --------------- | ------------------------------------ |
| `toFixed(n)`    | Formats number to `n` decimal places |
| `Math.round()`  | Rounds to nearest integer            |
| `Math.floor()`  | Rounds down                          |
| `Math.ceil()`   | Rounds up                            |
| `Math.random()` | Generates random number 0–1          |

```javascript
console.log(Math.round(3.6)); // 4
console.log(Math.floor(3.6)); // 3
console.log(Math.ceil(3.2));  // 4
console.log(Math.random());    // 0 ≤ x < 1
```

---

## 📝 Exercises

1. Create a string variable with your name. Print its length.
2. Create a number variable with your age. Round it using `Math.round()`.
3. Use a template literal to print: `"Name is Age years old."`
4. Check if a string contains a certain word using `includes()`.
5. Convert `"123"` to a number and add 10.
6. Generate a random number between 1 and 100.

---

# 🎯 Summary

* **Strings** store text; use `" "` or `' '` or `` ` ` `` (template literals).
* **Numbers** store numeric values; can be integers or decimals.
* Use **string methods** for manipulation: length, slice, trim, includes, repeat.
* Use **number methods** for formatting and calculations: Math.round, Math.floor, toFixed, random.
* Template literals simplify combining strings and numbers.


