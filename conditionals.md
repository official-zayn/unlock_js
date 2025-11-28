# 🔀 JavaScript Conditionals

Conditionals allow your program to **make decisions**.  
They let you run different code depending on conditions (true or false).

JavaScript provides:

1. `if`  
2. `if...else`  
3. `else if`  
4. `switch`  
5. Ternary operator (short form)

---

# 1️⃣ The `if` Statement

Runs code **only if** the condition is true.

```javascript
let age = 18;

if (age >= 18) {
  console.log("You are an adult.");
}
````

---

# 2️⃣ The `if...else` Statement

Runs one block if the condition is true,
otherwise runs the second block.

```javascript
let age = 16;

if (age >= 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}
```

---

# 3️⃣ The `else if` Ladder

Used when you have **multiple** conditions.

```javascript
let score = 75;

if (score >= 90) {
  console.log("Grade A");
} else if (score >= 70) {
  console.log("Grade B");
} else if (score >= 50) {
  console.log("Grade C");
} else {
  console.log("Fail");
}
```

---

# 4️⃣ The `switch` Statement

Useful when checking **multiple fixed values**.

```javascript
let day = 2;

switch (day) {
  case 1:
    console.log("Monday");
    break;
  case 2:
    console.log("Tuesday");
    break;
  case 3:
    console.log("Wednesday");
    break;
  default:
    console.log("Not a valid day");
}
```

### Notes:

* `break` prevents running the next case.
* `default` runs when no case matches.

---

# 5️⃣ Ternary Operator (Short `if-else`)

Compact way of writing simple conditions.

```javascript
let age = 20;
let result = age >= 18 ? "Adult" : "Minor";

console.log(result);
```

---

# ⭐ Real Examples

### Example 1: Even or Odd

```javascript
let num = 7;

if (num % 2 === 0) {
  console.log("Even");
} else {
  console.log("Odd");
}
```

---

### Example 2: Check Login Status

```javascript
let isLoggedIn = false;

if (!isLoggedIn) {
  console.log("Please log in.");
}
```

---

### Example 3: Switch with Strings

```javascript
let color = "red";

switch (color) {
  case "red":
    console.log("Stop!");
    break;
  case "yellow":
    console.log("Ready!");
    break;
  case "green":
    console.log("Go!");
    break;
  default:
    console.log("Unknown color");
}
```

---

# 📝 Exercises

### **Exercise 1**

Write an `if...else` that checks:

* If a number is positive
* If it is negative

### **Exercise 2**

Write an `else if` chain that prints:

* `"Cold"` if temp < 15
* `"Warm"` if temp < 30
* `"Hot"` otherwise

### **Exercise 3**

Use a switch to print the month name (1–12).

### **Exercise 4**

Use a ternary operator to check if a number is greater than 100.

### **Exercise 5**

Predict the output:

```javascript
let x = 10;

if (x > 5) {
  x -= 3;
} else {
  x += 3;
}

console.log(x);
```

---

# 🎉 Summary

* Conditionals control *decision-making* in your code.
* Use `if` for simple decisions.
* Use `else if` for multiple conditions.
* Use `switch` for checking many fixed values.
* Use the ternary operator for short checks.


