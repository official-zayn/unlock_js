# 📝 Form Handling & Validation in JavaScript

Form handling is one of the most important skills in web development.  
JavaScript allows you to **capture user input**, **validate it**, and **provide feedback** before submitting the form.

This ensures data is correct, complete, and secure.

---

## 1️⃣ Accessing Form Inputs

You can access form fields using `document.getElementById()` or `querySelector()`.

```html
<input type="text" id="username" />
````

```javascript
const username = document.getElementById("username").value;
console.log(username);
```

---

## 2️⃣ Listening for Form Submission

Use the `submit` event to handle the form before sending data.

```html
<form id="loginForm">
  <input type="text" id="email" />
  <button type="submit">Submit</button>
</form>
```

```javascript
const form = document.getElementById("loginForm");

form.addEventListener("submit", function (e) {
  e.preventDefault(); // Prevent automatic page reload
  console.log("Form submitted!");
});
```

---

## 3️⃣ Basic Form Validation

### Example: Checking for Empty Fields

```javascript
const emailInput = document.getElementById("email");

form.addEventListener("submit", function (e) {
  e.preventDefault();

  if (emailInput.value.trim() === "") {
    alert("Email is required!");
    return;
  }

  alert("Form is valid!");
});
```

---

## 4️⃣ Email Validation (RegEx)

```javascript
const email = emailInput.value;
const pattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

if (!pattern.test(email)) {
  alert("Please enter a valid email address");
  return;
}
```

---

## 5️⃣ Showing Error Messages on the Page

```html
<p id="error" style="color: red;"></p>
```

```javascript
const error = document.getElementById("error");

if (emailInput.value === "") {
  error.textContent = "Email cannot be empty.";
} else {
  error.textContent = "";
}
```

---

## 6️⃣ Password Validation Example

Common rules:

* Minimum length
* Must include numbers
* Must include uppercase/lowercase characters

```javascript
const password = document.getElementById("password").value;

if (password.length < 6) {
  error.textContent = "Password must be at least 6 characters.";
}
```

---

## 7️⃣ Real-Time Validation (Input Event)

```javascript
emailInput.addEventListener("input", function () {
  if (emailInput.value.includes("@")) {
    emailInput.style.borderColor = "green";
  } else {
    emailInput.style.borderColor = "red";
  }
});
```

---

## 8️⃣ Preventing Form Submission Until Valid

```javascript
form.addEventListener("submit", (e) => {
  if (emailInput.value === "" || password.value === "") {
    e.preventDefault();
    alert("Please fill in all fields.");
  }
});
```

---

## 9️⃣ Validation Summary

| Validation Type      | Example              |
| -------------------- | -------------------- |
| Empty field check    | `if (value === "")`  |
| Email format         | RegEx                |
| Password strength    | Length, characters   |
| Real-time validation | `input` event        |
| Blocking submission  | `e.preventDefault()` |

---

## 🧪 Practice Exercise

Create a form with:

* Full name
* Email
* Password
* Confirm password

Requirements:

* No field should be empty
* Email must be valid
* Password must be at least 6 characters
* Password and confirm password must match
* Show success or error messages on the screen

---

## 🎯 Summary

Form handling & validation allows you to:

* Capture user input
* Check for errors
* Improve user experience
* Prevent invalid data
* Build secure and interactive web forms

Mastering this topic is essential before moving into advanced web apps such as login systems, dashboards, and online tools.
