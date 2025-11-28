# 🧪 Unit Testing Basics in JavaScript

**Unit testing** is the process of testing **individual functions or components** to ensure they work as expected.  
Testing helps **catch errors early, improve reliability, and maintain clean code**.

---

## 1️⃣ Why Unit Testing?

- Verifies that **code works correctly**.  
- Detects **bugs early** in development.  
- Simplifies **refactoring and updates**.  
- Improves **code confidence and reliability**.

---

## 2️⃣ Simple Unit Test Without Libraries

```javascript
function add(a, b) {
  return a + b;
}

// Test function
function testAdd() {
  const result = add(2, 3);
  if (result === 5) {
    console.log("✅ Test Passed");
  } else {
    console.error("❌ Test Failed: Expected 5, got", result);
  }
}

testAdd();
````

* Simple `if` check to validate function output
* Prints **pass/fail** messages in console

---

## 3️⃣ Using Assertions (Vanilla JS)

```javascript
function assertEqual(actual, expected, testName) {
  if (actual === expected) {
    console.log(`✅ ${testName}`);
  } else {
    console.error(`❌ ${testName} - Expected ${expected}, got ${actual}`);
  }
}

function multiply(a, b) {
  return a * b;
}

// Run test
assertEqual(multiply(2, 3), 6, "Multiply 2 * 3");
assertEqual(multiply(5, 0), 0, "Multiply 5 * 0");
```

* Makes **tests more readable and reusable**

---

## 4️⃣ Using Jest (Popular JS Testing Library)

1. Install Jest:

```bash
npm install --save-dev jest
```

2. Create `math.js`:

```javascript
function add(a, b) {
  return a + b;
}

module.exports = add;
```

3. Create `math.test.js`:

```javascript
const add = require('./math');

test('adds 2 + 3 to equal 5', () => {
  expect(add(2, 3)).toBe(5);
});
```

4. Run tests:

```bash
npx jest
```

* Jest provides **clear syntax, assertions, and test reports**

---

## 5️⃣ Practical Tips

* Test **small, isolated units** (functions, components).
* Include **edge cases** and unexpected inputs.
* Use **descriptive test names**.
* Run tests frequently to **catch regressions early**.

---

## 📝 Exercises

1. Write a unit test for a function that returns the square of a number.
2. Test a function that capitalizes the first letter of a string.
3. Write tests for an array-sum function with normal and empty arrays.
4. Use Jest to test a function that checks if a number is even.
5. Write a test for a function that returns the largest number in an array.

---

# 🎯 Summary

* Unit testing ensures **code correctness and reliability**.
* Use **manual assertions** or **testing frameworks** like Jest.
* Test **functions independently**, including edge cases.
* Essential for **maintaining large-scale projects** and building confidence in your code.


