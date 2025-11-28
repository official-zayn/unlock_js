# 🗂️ JavaScript Arrays

Arrays are **ordered lists of values**.  
They allow you to store **multiple items** in a single variable.

---

## 1️⃣ Creating an Array

```javascript
// Using square brackets
let fruits = ["apple", "banana", "orange"];

// Empty array
let numbers = [];
````

---

## 2️⃣ Accessing Array Items

Array items are **indexed starting at 0**.

```javascript
console.log(fruits[0]); // "apple"
console.log(fruits[2]); // "orange"
```

---

## 3️⃣ Modifying Arrays

### Change an element

```javascript
fruits[1] = "mango";
console.log(fruits); // ["apple", "mango", "orange"]
```

### Add items

```javascript
fruits.push("grape"); // add at the end
fruits.unshift("kiwi"); // add at the start
```

### Remove items

```javascript
fruits.pop(); // removes last
fruits.shift(); // removes first
```

---

## 4️⃣ Array Properties & Methods

| Method/Property                        | Description                  |
| -------------------------------------- | ---------------------------- |
| `length`                               | Number of items in the array |
| `indexOf(value)`                       | Returns the index of a value |
| `includes(value)`                      | Returns true if value exists |
| `slice(start, end)`                    | Returns a new array (copy)   |
| `splice(start, deleteCount, items...)` | Add/remove items             |

### Examples

```javascript
console.log(fruits.length); // 4
console.log(fruits.indexOf("mango")); // 1
console.log(fruits.includes("banana")); // false
```

---

## 5️⃣ Looping Through Arrays

```javascript
// Using for loop
for (let i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}

// Using for...of
for (let fruit of fruits) {
  console.log(fruit);
}
```

---

## 6️⃣ Multi-dimensional Arrays

Arrays can hold **arrays**.

```javascript
let matrix = [
  [1, 2],
  [3, 4],
  [5, 6]
];

console.log(matrix[1][0]); // 3
```

---

## 📝 Exercises

1. Create an array of your 5 favorite movies.
2. Add one movie to the beginning and one to the end.
3. Remove the second movie.
4. Print all movies using a loop.
5. Check if a specific movie exists using `includes()`.

---

# 🎯 Summary

* Arrays store **multiple values in order**.
* Access items with **index**.
* Modify using **push, pop, shift, unshift**.
* Use loops to process arrays.
* Arrays can be **multi-dimensional**.

