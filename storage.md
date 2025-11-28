# 💾 Local Storage & Session Storage in JavaScript

Web browsers provide two powerful tools for storing data directly on the client side:

- **Local Storage**
- **Session Storage**

These allow your application to **save data** even after refresh, keeping user preferences, app state, or small databases.

---

# 1️⃣ What is Web Storage?

Web Storage provides **key-value storage** inside the browser.

| Feature | Local Storage | Session Storage |
|--------|----------------|-----------------|
| Persistence | Until manually cleared | Clears when tab closes |
| Storage Limit | ~5–10MB | ~5MB |
| Use Cases | Preferences, settings, notes, apps | Temporary form data, session states |

Both storage types use the same API.

---

# 2️⃣ Using Local Storage

### ✔️ Store (Save) Data

```javascript
localStorage.setItem("username", "Abideen");
````

### ✔️ Get (Retrieve) Data

```javascript
const name = localStorage.getItem("username");
console.log(name); // "Abideen"
```

### ✔️ Remove a Single Item

```javascript
localStorage.removeItem("username");
```

### ✔️ Clear Everything

```javascript
localStorage.clear();
```

---

# 3️⃣ Storing Objects & Arrays (Important!)

Local Storage only stores **strings**.
To store objects or arrays, use `JSON.stringify()`.

### Save an Object

```javascript
const user = {
  name: "Abideen",
  role: "Developer",
  theme: "dark"
};

localStorage.setItem("user", JSON.stringify(user));
```

### Retrieve and Convert Back

```javascript
const userData = JSON.parse(localStorage.getItem("user"));
console.log(userData.name);
```

---

# 4️⃣ Using Session Storage

Session Storage works exactly like Local Storage but clears when the tab closes.

### Save

```javascript
sessionStorage.setItem("token", "abc123");
```

### Retrieve

```javascript
const token = sessionStorage.getItem("token");
```

### Remove

```javascript
sessionStorage.removeItem("token");
```

### Clear All

```javascript
sessionStorage.clear();
```

---

# 5️⃣ Practical Use Cases

### 📝 1. Todo App (Save tasks permanently)

* Save tasks to Local Storage
* Load them again on page refresh
* Remove tasks and update storage

### 💡 2. User Preferences

* Theme (dark/light)
* Language settings
* Layout preferences

### 📄 3. Form Autosave (Session Storage)

* Temporarily store form inputs
* Prevent losing data when page refreshes unexpectedly

---

# 6️⃣ Example: Saving Form Input Automatically

```javascript
// Save input on typing
const input = document.querySelector("#email");

input.addEventListener("input", () => {
  localStorage.setItem("email", input.value);
});

// Restore on load
window.addEventListener("DOMContentLoaded", () => {
  input.value = localStorage.getItem("email") || "";
});
```

---

# 🎯 Summary

* **Local Storage** → persistent data until cleared
* **Session Storage** → temporary data until tab closes
* Uses simple key-value methods:
  `setItem`, `getItem`, `removeItem`, `clear`
* Use `JSON.stringify()` and `JSON.parse()` to store objects
* Perfect for todos, notes, user preferences, and temporary form data

---

# 🧪 Mini Exercise

1. Create a text field that saves user input to Local Storage.
2. Display the saved value even after refreshing the page.
3. Add a "Clear" button to remove stored data.

