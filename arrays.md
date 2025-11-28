# 🗂️ JavaScript Arrays

Arrays are **ordered lists of values**.  
They allow you to store **multiple items** in a single variable and work with them efficiently.

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
fruits.push("grape");     // add at the end
fruits.unshift("kiwi");   // add at the start
```

### Remove items

```javascript
fruits.pop();   // removes last
fruits.shift(); // removes first
```

---

## 4️⃣ Array Properties & Methods

| Method/Property                        | Description                  |
| -------------------------------------- | ---------------------------- |
| `length`                               | Number of items in the array |
| `indexOf(value)`                       | Returns the index of a value |
| `includes(value)`                      | Returns true if value exists |
| `slice(start,end)`                     | Returns a new array (copy)   |
| `splice(start, deleteCount, items...)` | Add/remove items             |

### Examples

```javascript
console.log(fruits.length);           // 4
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

## 6️⃣ Array Methods (`forEach`, `map`, `filter`, `reduce`)

### forEach → iterate without returning

```javascript
fruits.forEach(fruit => console.log(fruit));
```

### map → transform each element

```javascript
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8]
```

### filter → select elements

```javascript
const evens = numbers.filter(num => num % 2 === 0);
console.log(evens); // [2, 4]
```

### reduce → accumulate a single value

```javascript
const sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // 10
```

---

## 7️⃣ Multi-dimensional Arrays

Arrays can hold **arrays**.

```javascript
const matrix = [
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
4. Print all movies using a loop and using `forEach()`.
5. Create a numbers array `[1,2,3,4,5]`.

   * Double the numbers using `map()`.
   * Select even numbers using `filter()`.
   * Find the sum of all numbers using `reduce()`.
6. Create a 2D array representing a 3x3 grid and print the center value.

---

# 🎯 Summary

* Arrays store **multiple values in order**.
* Access items with **index** and modify with `push`, `pop`, `shift`, `unshift`.
* Loop through arrays using `for`, `for...of`, or `forEach()`.
* Use **array methods** for common operations: `map()`, `filter()`, `reduce()`.
* Arrays can be **multi-dimensional** for structured data.
