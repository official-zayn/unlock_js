# 🧩 JavaScript Objects

Objects are **collections of key–value pairs**.  
They allow you to store **related data** in a single structure.

---

## 1️⃣ Creating an Object

```javascript
// Using object literal
let person = {
  name: "Abideen",
  age: 25,
  isStudent: true
};

// Empty object
let car = {};
````

---

## 2️⃣ Accessing Object Properties

### Dot notation

```javascript
console.log(person.name); // "Abideen"
```

### Bracket notation

```javascript
console.log(person["age"]); // 25
```

---

## 3️⃣ Modifying Objects

### Add a new property

```javascript
person.country = "Nigeria";
```

### Update a property

```javascript
person.age = 26;
```

### Delete a property

```javascript
delete person.isStudent;
```

---

## 4️⃣ Object Methods

Objects can have **functions as values**, called **methods**.

```javascript
let person = {
  name: "Abideen",
  greet: function() {
    console.log("Hello, " + this.name);
  }
};

person.greet(); // "Hello, Abideen"
```

> `this` refers to the current object.

---

## 5️⃣ Looping Through Objects

Use **for...in** to iterate over properties:

```javascript
for (let key in person) {
  console.log(key + ":", person[key]);
}
```

---

## 6️⃣ Nested Objects

Objects can contain **other objects**:

```javascript
let student = {
  name: "Tunde",
  address: {
    city: "Lagos",
    zip: "100001"
  }
};

console.log(student.address.city); // "Lagos"
```

---

## 📝 Exercises

1. Create an object `book` with properties: `title`, `author`, `pages`.
2. Add a new property `year`.
3. Change the `pages` value.
4. Add a method `summary()` that prints: `"Title by Author"`.
5. Loop through all properties and print keys and values.

---

# 🎯 Summary

* Objects store **related data as key–value pairs**.
* Access using **dot** or **bracket** notation.
* Objects can have **methods** (functions).
* Use **for...in** to loop through properties.
* Objects can be **nested** for structured data.

