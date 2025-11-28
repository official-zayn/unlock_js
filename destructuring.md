# 🔍 Destructuring, Spread & Rest in JavaScript

Destructuring and the Spread/Rest operators are powerful ES6 features that make your code **cleaner, shorter, and easier to read**.  
They are used to extract values, combine data, and handle flexible numbers of arguments.

---

# 1️⃣ Array Destructuring

Extract values from arrays into variables:

```javascript
const numbers = [10, 20, 30];

const [a, b, c] = numbers;

console.log(a); // 10
console.log(b); // 20
console.log(c); // 30
````

### Skip values:

```javascript
const [first, , third] = [1, 2, 3];
console.log(first, third); // 1 3
```

### Default values:

```javascript
const [name = "Guest"] = [];
console.log(name); // Guest
```

---

# 2️⃣ Object Destructuring

Extract properties from objects:

```javascript
const user = {
  name: "Ayo",
  age: 25,
  city: "Lagos"
};

const { name, age } = user;

console.log(name); // Ayo
console.log(age);  // 25
```

### Rename variables:

```javascript
const { city: location } = user;
console.log(location); // Lagos
```

### Default values:

```javascript
const { role = "User" } = {};
console.log(role); // User
```

---

# 3️⃣ Nested Destructuring

For objects inside objects or arrays inside arrays:

```javascript
const profile = {
  username: "jsMaster",
  details: {
    email: "test@example.com",
    followers: 1200
  }
};

const {
  details: { email, followers }
} = profile;

console.log(email, followers); // test@example.com 1200
```

---

# 4️⃣ Spread Operator (`...`) – Expand Values

### Spread in arrays:

```javascript
const a = [1, 2];
const b = [3, 4];

const combined = [...a, ...b];
console.log(combined); // [1, 2, 3, 4]
```

### Spread in objects:

```javascript
const user1 = { name: "Ayo", age: 25 };
const update = { age: 26, city: "Lagos" };

const newUser = { ...user1, ...update };
console.log(newUser);
// { name: "Ayo", age: 26, city: "Lagos" }
```

---

# 5️⃣ Rest Operator (`...`) – Collect Remaining Values

### Rest in arrays:

```javascript
const [first, ...rest] = [1, 2, 3, 4];
console.log(rest); // [2, 3, 4]
```

### Rest in objects:

```javascript
const { name, ...others } = {
  name: "Ayo",
  age: 25,
  city: "Lagos"
};

console.log(others);
// { age: 25, city: "Lagos" }
```

### Rest in functions:

```javascript
function sum(...nums) {
  return nums.reduce((acc, n) => acc + n, 0);
}

console.log(sum(1, 2, 3, 4)); // 10
```

---

# 🧠 When to Use These Features

Use **destructuring** when:

* You want cleaner access to array or object values
* You want to extract only the needed parts
* You want default values or renaming

Use **spread operator** when:

* Merging arrays or objects
* Copying data
* Passing dynamic values into functions

Use **rest operator** when:

* Accepting unlimited arguments
* Capturing "remaining values" from arrays/objects

---

# 📝 Practice Exercises

### 1. Array Destructuring

Extract the first two colors:

```javascript
const colors = ["red", "green", "blue"];
```

### 2. Object Destructuring

Extract `title` and rename `author` to `writer`:

```javascript
const book = { title: "JS Guide", author: "John Doe", year: 2024 };
```

### 3. Spread Operator

Merge these arrays:

```javascript
const a = [1, 2];
const b = [3, 4];
```

### 4. Rest Operator

Create a function that multiplies all numbers passed into it.

---

This topic prepares you for **cleaner code**, advanced APIs, React development, and modular JavaScript.
