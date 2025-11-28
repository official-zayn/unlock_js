# 🔍 Regular Expressions (RegEx) in JavaScript

**Regular Expressions (RegEx)** are patterns used to **match, search, and manipulate strings**.  
They are essential for **validation, parsing, and text processing** in web applications.

---

## 1️⃣ Creating Regular Expressions

There are **two ways**:

```javascript
// 1. Literal syntax
const regex1 = /hello/;

// 2. Constructor syntax
const regex2 = new RegExp("hello");
````

* `/pattern/` → simple and common
* `new RegExp()` → useful for dynamic patterns

---

## 2️⃣ Basic Methods

```javascript
const str = "Hello World";

console.log(/Hello/.test(str));   // true (match found)
console.log(str.match(/World/));  // ["World"]
console.log(str.replace(/World/, "JS")); // "Hello JS"
console.log(str.search(/Hello/)); // 0 (index)
```

* `.test()` → checks if pattern exists
* `.match()` → returns matched text
* `.replace()` → replace matched text
* `.search()` → index of match

---

## 3️⃣ Special Characters

| Symbol | Meaning                           |             |
| ------ | --------------------------------- | ----------- |
| `.`    | Any single character              |             |
| `\d`   | Any digit `[0-9]`                 |             |
| `\w`   | Any word character `[a-zA-Z0-9_]` |             |
| `\s`   | Any whitespace                    |             |
| `^`    | Start of string                   |             |
| `$`    | End of string                     |             |
| `*`    | 0 or more repetitions             |             |
| `+`    | 1 or more repetitions             |             |
| `?`    | 0 or 1 occurrence                 |             |
| `[]`   | Character set                     |             |
| `      | `                                 | OR operator |
| `()`   | Grouping                          |             |

---

## 4️⃣ Quantifiers and Flags

```javascript
const str = "aaaabbbb";

console.log(str.match(/a+/g));  // ["aaaa"]
console.log(str.match(/b{2}/g)); // ["bb", "bb"]
```

* `g` → global match (all occurrences)
* `i` → case-insensitive
* `m` → multiline

---

## 5️⃣ Practical Examples

### Validate an Email

```javascript
const emailRegex = /^[a-zA-Z0-9._%+-]+@[a-z0-9.-]+\.[a-z]{2,}$/;
console.log(emailRegex.test("test@example.com")); // true
console.log(emailRegex.test("invalid-email"));    // false
```

### Validate a Phone Number (10 digits)

```javascript
const phoneRegex = /^\d{10}$/;
console.log(phoneRegex.test("0801234567")); // true
console.log(phoneRegex.test("12345"));     // false
```

### Extract All Numbers from a String

```javascript
const str = "I have 2 apples and 10 oranges";
const numbers = str.match(/\d+/g);
console.log(numbers); // ["2", "10"]
```

---

## 📝 Exercises

1. Create a regex to match all words starting with "J" in a string.
2. Validate if a string is a proper email address.
3. Extract all digits from a sentence and sum them.
4. Replace all spaces in a string with hyphens using regex.
5. Match strings that end with `.com` or `.org`.

---

# 🎯 Summary

* RegEx is **a powerful tool to handle strings**.
* Methods: `.test()`, `.match()`, `.replace()`, `.search()`
* Flags: `g` (global), `i` (case-insensitive), `m` (multiline)
* Use for **validation, parsing, and text manipulation** in web apps.


