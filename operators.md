# ➗ JavaScript Operators

Operators allow you to **perform actions on values and variables**.  
Think of them as tools for calculation, comparison, or logic.

JavaScript has several categories of operators:

1. Arithmetic Operators  
2. Assignment Operators  
3. Comparison Operators  
4. Logical Operators  
5. String Operators  
6. Unary Operators  
7. Ternary Operator  
8. Type Operators  

---

# 1️⃣ Arithmetic Operators

Used to perform mathematical calculations.

| Operator | Meaning        | Example |
|----------|----------------|---------|
| `+`      | Addition       | `5 + 2` |
| `-`      | Subtraction    | `5 - 2` |
| `*`      | Multiplication | `5 * 2` |
| `/`      | Division       | `10 / 2` |
| `%`      | Modulus (Remainder) | `10 % 3` |
| `**`     | Exponent       | `2 ** 3` |

### Example
```javascript
let x = 10;
let y = 3;

console.log(x + y); // 13
console.log(x % y); // 1
console.log(2 ** 4); // 16
````

---

# 2️⃣ Assignment Operators

Used to assign values to variables.

| Operator | Meaning           | Example  |
| -------- | ----------------- | -------- |
| `=`      | Assign value      | `x = 10` |
| `+=`     | Add & assign      | `x += 5` |
| `-=`     | Subtract & assign | `x -= 3` |
| `*=`     | Multiply & assign | `x *= 2` |
| `/=`     | Divide & assign   | `x /= 2` |
| `%=`     | Modulus & assign  | `x %= 3` |

### Example

```javascript
let x = 10;
x += 5; // 15
```

---

# 3️⃣ Comparison Operators

Used to compare values.
Always return a **boolean** (`true` or `false`).

| Operator | Meaning           | Example        |
| -------- | ----------------- | -------------- |
| `==`     | Equal (loose)     | `"5" == 5` ✔️  |
| `===`    | Strict equal      | `"5" === 5` ❌  |
| `!=`     | Not equal (loose) | `"5" != 5` ❌   |
| `!==`    | Strict not equal  | `"5" !== 5` ✔️ |
| `>`      | Greater than      | `10 > 5`       |
| `<`      | Less than         | `3 < 9`        |
| `>=`     | Greater or equal  | `10 >= 10`     |
| `<=`     | Less or equal     | `7 <= 8`       |

### Example

```javascript
console.log(5 == "5");   // true
console.log(5 === "5");  // false
```

---

# 4️⃣ Logical Operators

Used in conditions (`if` statements).

| Operator | Meaning | Example                 |    |       |   |               |
| -------- | ------- | ----------------------- | -- | ----- | - | ------------- |
| `&&`     | AND     | `true && false` = false |    |       |   |               |
| `\|\|`  | OR | `true |   | false` = true |
| `!`      | NOT     | `!true` = false         |    |       |   |               |

### Example

```javascript
let age = 20;
console.log(age >= 18 && age <= 30); // true
```

---

# 5️⃣ String Operator

The `+` operator concatenates (joins) strings.

```javascript
let first = "Ultra";
let second = "Adetech";

console.log(first + " " + second);
// Ultra Adetech
```

---

# 6️⃣ Unary Operators

Operators with just **one operand**.

| Operator | Meaning           | Example |
| -------- | ----------------- | ------- |
| `++`     | Increment         | `x++`   |
| `--`     | Decrement         | `x--`   |
| `+`      | Convert to number | `+"5"`  |
| `-`      | Negate value      | `-10`   |

### Example

```javascript
let x = 5;
x++;
console.log(x); // 6
```

---

# 7️⃣ Ternary Operator

Short version of an `if/else` statement.

```javascript
let age = 18;
let result = age >= 18 ? "Adult" : "Minor";

console.log(result);
```

---

# 8️⃣ Type Operators

### `typeof`

Returns the data type.

```javascript
typeof 100; // "number"
```

### `instanceof`

Checks if an object belongs to a particular class.

```javascript
[] instanceof Array; // true
```

---

# 🧪 Practical Examples

### Example 1: Math + Comparison

```javascript
let score = 45;
console.log(score + 5 > 50); // false
```

### Example 2: Using logical operators

```javascript
let loggedIn = true;
let isAdmin = false;

if (loggedIn && !isAdmin) {
  console.log("Access limited");
}
```

---

# 📝 Exercises

### **Exercise 1**

Use arithmetic operators to calculate:

* Sum of 12 and 8
* Remainder of 19 ÷ 4
* `3` raised to power `5`

### **Exercise 2**

Write a comparison that returns **true** and one that returns **false**.

### **Exercise 3**

Use logical operators:

```javascript
let age = 17;
```

Check if age is between 13 and 19 (teenager).

### **Exercise 4**

Predict the output:

```javascript
let x = 10;
x *= 2;
x -= 5;
console.log(x);
```

### **Exercise 5**

Use the ternary operator to check:

* If a number is even or odd.

---

# 🎉 Summary

* Operators perform actions on variables and values.
* Arithmetic, comparison, logical, and assignment operators are used most frequently.
* Ternary operator simplifies conditional logic.
* `typeof` helps check variable types.

