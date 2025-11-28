# 🔁 Loops in JavaScript

Loops allow you to **repeat a block of code** multiple times. They are essential when working with lists, running repeated tasks, or processing data.

JavaScript provides several loop types, each with its specific use case.

---

## 1️⃣ `for` Loop

Used when you **know how many times** you want to repeat a task.

### **Syntax**

```js
for (initialization; condition; update) {
  // code to run
}
```

### **Example**

```js
for (let i = 1; i <= 5; i++) {
  console.log("Number:", i);
}
```

---

## 2️⃣ `while` Loop

Runs as long as the condition remains **true**.

### **Example**

```js
let count = 1;

while (count <= 3) {
  console.log(count);
  count++;
}
```

---

## 3️⃣ `do...while` Loop

This loop runs **at least once**, even if the condition is false.

### **Example**

```js
let num = 1;

do {
  console.log(num);
  num++;
} while (num <= 3);
```

---

## 4️⃣ `for...of` Loop

Used to loop through **arrays** and other iterable objects.

### **Example**

```js
const fruits = ["apple", "banana", "orange"];

for (const fruit of fruits) {
  console.log(fruit);
}
```

---

## 5️⃣ `for...in` Loop

Used to loop through the **keys** of an object.

### **Example**

```js
const user = { name: "Ayo", age: 22 };

for (const key in user) {
  console.log(key, ":", user[key]);
}
```

---

## 🧩 Summary Table

| Loop Type    | Best Used For                  |
| ------------ | ------------------------------ |
| `for`        | Fixed number of repetitions    |
| `while`      | Repeat until condition changes |
| `do...while` | Must run at least once         |
| `for...of`   | Arrays / Iterables             |
| `for...in`   | Object keys                    |

---

## 📝 Exercises

Try these for practice:

1. Print numbers from **1 to 10** using a `for` loop.
2. Count down from **5 to 1** using a `while` loop.
3. Use `for...of` to print all items in this array:

   ```js
   const colors = ["red", "green", "blue"];
   ```
4. Use `for...in` to print all keys and values of this object:

   ```js
   const car = { brand: "Toyota", model: "Corolla" };
   ```
5. Print your name **3 times** using any loop type.

