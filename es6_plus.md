# ⚡ ES6+ Features Not Covered Yet

ES6+ introduced many **modern JavaScript features** that make code cleaner, safer, and more readable.  
This lesson covers some **less common but powerful features**.

---

## 1️⃣ Optional Chaining (`?.`)

- Safely access **nested properties** without errors if a property is `undefined` or `null`.

```javascript
const user = { name: "Abideen", address: { city: "Lagos" } };

console.log(user.address?.city);      // "Lagos"
console.log(user.contact?.phone);     // undefined (no error)
````

* Prevents `TypeError` when accessing deep objects.

---

## 2️⃣ Nullish Coalescing (`??`)

* Provides a **default value** only if the variable is `null` or `undefined`.

```javascript
let username = null;
let displayName = username ?? "Guest";
console.log(displayName); // "Guest"

username = "";
displayName = username ?? "Guest";
console.log(displayName); // "" (empty string is not nullish)
```

---

## 3️⃣ BigInt

* Handle **very large integers** beyond `Number.MAX_SAFE_INTEGER`.

```javascript
const bigNumber = 9007199254740991n;
const biggerNumber = bigNumber + 1n;
console.log(biggerNumber); // 9007199254740992n
```

* Note the `n` at the end of the number.

---

## 4️⃣ `Set` and `Map`

### Set

* Store **unique values** only:

```javascript
const numbers = new Set([1, 2, 2, 3]);
console.log(numbers); // Set {1, 2, 3}
```

### Map

* Store **key-value pairs** with any type as key:

```javascript
const capitals = new Map();
capitals.set("Nigeria", "Abuja");
capitals.set("France", "Paris");

console.log(capitals.get("France")); // "Paris"
```

---

## 5️⃣ Dynamic Property Names

* Use **computed property names** in objects:

```javascript
const key = "email";
const user = {
  name: "Abideen",
  [key]: "abideen@example.com"
};

console.log(user.email); // "abideen@example.com"
```

---

## 6️⃣ Template Literal Tags (Advanced)

* Customize **template strings** with functions:

```javascript
function highlight(strings, ...values) {
  return strings.reduce((result, str, i) => `${result}${str}<b>${values[i] || ''}</b>`, '');
}

const name = "Tunde";
const message = highlight`Hello ${name}, welcome!`;
console.log(message); // "Hello <b>Tunde</b>, welcome!"
```

---

## 📝 Exercises

1. Access a deeply nested property using **optional chaining**.
2. Provide a default value using **nullish coalescing** for a possibly undefined variable.
3. Create a `BigInt` number and perform arithmetic with it.
4. Use a `Set` to remove duplicates from an array.
5. Use a `Map` to store and retrieve multiple country-capital pairs.
6. Use **dynamic property names** to create an object from user input.

---

# 🎯 Summary

* ES6+ features improve **readability, safety, and functionality**.
* Optional chaining and nullish coalescing prevent errors and simplify defaults.
* BigInt, Set, and Map expand the capabilities of JS data handling.
* Dynamic property names and template tags allow **more flexible, dynamic code**.


