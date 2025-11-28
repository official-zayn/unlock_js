# 📄 JSON Deep Dive in JavaScript

**JSON (JavaScript Object Notation)** is a lightweight format for **storing and exchanging data**.  
It is widely used in web development for APIs, configuration files, and local storage.

---

## 1️⃣ What is JSON?

- JSON is a **text-based format**.  
- Can represent **objects** (`{}`) and **arrays** (`[]`).  
- Keys must be **strings**, values can be:  
  - Number, String, Boolean, Null, Object, Array  

```json
{
  "name": "Abideen",
  "age": 25,
  "skills": ["JavaScript", "HTML", "CSS"],
  "isStudent": false
}
````

---

## 2️⃣ Converting Between JSON and JavaScript

### Parsing JSON → JavaScript object

```javascript
const jsonString = '{"name":"Abideen","age":25}';
const user = JSON.parse(jsonString);
console.log(user.name); // "Abideen"
```

### Stringifying JavaScript object → JSON

```javascript
const userObj = { name: "Tunde", age: 30 };
const jsonStr = JSON.stringify(userObj);
console.log(jsonStr); // '{"name":"Tunde","age":30}'
```

---

## 3️⃣ Nested JSON

JSON can contain objects and arrays inside each other:

```json
{
  "company": "UltraAdetech",
  "employees": [
    { "name": "Abideen", "role": "Developer" },
    { "name": "Tunde", "role": "Designer" }
  ]
}
```

Access nested data in JavaScript:

```javascript
const data = {
  company: "UltraAdetech",
  employees: [
    { name: "Abideen", role: "Developer" },
    { name: "Tunde", role: "Designer" }
  ]
};

console.log(data.employees[0].name); // "Abideen"
```

---

## 4️⃣ Practical Uses

* **APIs**: Fetch data from a server and parse JSON.
* **Local Storage**: Store complex objects by stringifying them.
* **Configuration files**: JSON is used for settings in web apps.

---

## 5️⃣ Working with JSON in Arrays

```javascript
const usersJSON = '[{"name":"A","age":20},{"name":"B","age":25}]';
const users = JSON.parse(usersJSON);

users.forEach(user => console.log(user.name)); // "A" "B"
```

---

## 📝 Exercises

1. Convert this JSON string to a JS object and log the `name` property:

   ```json
   '{"name":"Tunde","age":28,"skills":["JS","HTML"]}'
   ```
2. Create a JS object for a book (title, author, pages) and convert it to JSON.
3. Fetch JSON data from `https://jsonplaceholder.typicode.com/users` and log the names of all users.
4. Create a nested JSON for a class of students and access the second student's first name.
5. Store a JS object in `localStorage` using JSON and retrieve it later.

---

# 🎯 Summary

* JSON is **lightweight, text-based, and widely used** in web apps.
* Use `JSON.parse()` to convert JSON to JS objects.
* Use `JSON.stringify()` to convert JS objects to JSON.
* Nested JSON structures can be accessed using **dot notation and array indices**.
* Essential for **APIs, local storage, and data transfer**.
