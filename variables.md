# 🔤 JavaScript Variables

Variables are **containers that store data**.  
They allow your program to remember values and reuse them later.

In JavaScript, you create variables using:

- `var` (old — avoid using)
- `let` (recommended)
- `const` (recommended for values that do not change)

---

## 🟦 1. Declaring Variables

### Using `let`
```javascript
let age = 25;
````

### Using `const`

```javascript
const PI = 3.14;
```

### Using `var` (not recommended)

```javascript
var name = "Abideen";
```

---

## 🟩 2. Rules for Variable Names

You **can** use:

* Letters
* Numbers (not at the start)
* Underscore `_`
* Dollar sign `$`

You **cannot**:

* Start with a number
* Use spaces
* Use JavaScript keywords (`let`, `class`, `return`, etc.)

### Valid examples:

```javascript
let userName;
let total_amount;
let $price;
let count2;
```

### Invalid examples:

```javascript
let 2count;   // ❌ cannot start with a number
let user name; // ❌ no spaces
let class;     // ❌ keyword
```

---

## 🟧 3. `let` vs `const`

### `let` → value can change

```javascript
let score = 50;
score = 70; // ✔️ allowed
```

### `const` → value cannot change

```javascript
const country = "Nigeria";
country = "Ghana"; // ❌ error
```

Use **const by default**, and **let** only when the value will change.

---

## 🟪 4. Declaring Without Initial Value

You can create an empty variable:

```javascript
let age;
age = 18;
```

---

## 🟨 5. Multiple Variable Declarations

```javascript
let firstName = "Tunde",
    lastName = "Shittu",
    age = 25;
```

---

## 🧪 6. Examples

### Example 1: Storing a string

```javascript
let school = "OdumareTech";
```

### Example 2: Updating a value

```javascript
let count = 1;
count = 2;
```

### Example 3: Using const

```javascript
const website = "https://ultraadetech.com";
```

---

## 📝 7. Exercises

### **Exercise 1**

Create variables to store:

* Your name
* Your age
* Your favorite color

### **Exercise 2**

Create a `const` variable for:

* The value of pi
* Your country

### **Exercise 3**

Try creating invalid variable names and correct them.

### **Exercise 4**

Predict the output:

```javascript
let x = 10;
x = x + 5;
console.log(x);
```

---

## 🎉 Summary

* Variables store values.
* Use **let** for changing values.
* Use **const** for fixed values.
* Variable names must follow rules.

