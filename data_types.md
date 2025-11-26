# 🧩 JavaScript Data Types

Data types tell JavaScript **what kind of value** a variable holds.  
JavaScript has **primitive data types** and **complex data types**.

Understanding them helps you write correct and predictable code.

---

# 🎯 1. Primitive Data Types

Primitive types store **single, simple values**.

They include:

1. **String**
2. **Number**
3. **Boolean**
4. **Null**
5. **Undefined**
6. **BigInt**
7. **Symbol**

---

## 1️⃣ String  
Used for text.

```javascript
let name = "Abideen";
let city = 'Lagos';
````

Strings must be inside quotes.

---

## 2️⃣ Number

For integers and decimals.

```javascript
let age = 25;
let price = 19.99;
```

JavaScript does **not** separate integers and floats — both are `number`.

---

## 3️⃣ Boolean

Represents **true** or **false**.

```javascript
let isStudent = true;
let isLoggedIn = false;
```

Used in decision-making (`if` statements).

---

## 4️⃣ Null

A deliberate "empty" value.

```javascript
let result = null; // intentionally empty
```

---

## 5️⃣ Undefined

Means "not assigned yet."

```javascript
let score;
console.log(score); // undefined
```

---

## 6️⃣ BigInt

Used for extremely large numbers.

```javascript
let big = 9007199254740991n; // note the 'n'
```

---

## 7️⃣ Symbol (Advanced)

Used for unique identifiers.

```javascript
let id = Symbol("userID");
```

---

# 🧱 2. Complex Data Types

These store collections or structures of data.

* **Object**
* **Array**

---

## 8️⃣ Object

Stores data in **key–value pairs**.

```javascript
let user = {
  name: "Abideen",
  age: 25,
  location: "Lagos"
};
```

---

## 9️⃣ Array

Stores multiple values in a list.

```javascript
let colors = ["red", "green", "blue"];
```

Arrays are technically **objects**, but used differently.

---

# 🔍 Checking Data Types

Use the `typeof` operator:

```javascript
console.log(typeof "Hello");   // string
console.log(typeof 20);        // number
console.log(typeof true);      // boolean
console.log(typeof undefined); // undefined
console.log(typeof null);      // object (JavaScript bug)
console.log(typeof {});        // object
console.log(typeof []);        // object
```

Note:
`typeof null` returns **object** — a long-standing JavaScript quirk.

---

# 🧪 Examples

### Example 1: Different Types

```javascript
let name = "Tunde";     // string
let age = 22;           // number
let isAdmin = false;    // boolean
let salary = null;      // null
let level;              // undefined
```

### Example 2: Arrays & Objects

```javascript
let fruits = ["apple", "banana", "orange"];
let student = {
  name: "Ayo",
  grade: "A"
};
```

---

# 📝 Exercises

### **Exercise 1**

Create variables with these data types:

* String
* Number
* Boolean
* Null
* Undefined

### **Exercise 2**

Create an **array** of 5 colors.

### **Exercise 3**

Create an **object** with your:

* name
* age
* favorite language

### **Exercise 4**

Use `typeof` to check:

```javascript
let x = "50";
let y = 50;
let z = null;
```

### **Exercise 5**

Is `"true"` a boolean or a string? Try using it in code.

---

# 🎉 Summary

* Data types describe the **kind of value** stored in variables.
* JavaScript has **7 primitive** and **2 complex** types.
* Use `typeof` to check the type.
* Understanding data types helps prevent bugs.

