# 🌐 JavaScript DOM Manipulation

The **DOM (Document Object Model)** is the interface between JavaScript and your HTML.  
It allows you to **access, modify, and interact** with elements on the page.

DOM manipulation is essential for creating **interactive and dynamic web pages**.

---

## 1️⃣ Accessing Elements

### By ID
```javascript
const title = document.getElementById("title");
console.log(title.textContent);
````

### By Class Name

```javascript
const texts = document.getElementsByClassName("text");
console.log(texts[0].textContent);
```

### By Tag Name

```javascript
const paragraphs = document.getElementsByTagName("p");
console.log(paragraphs[0].textContent);
```

### Using `querySelector` / `querySelectorAll`

```javascript
const firstText = document.querySelector(".text");
const allTexts = document.querySelectorAll("p");
```

> `querySelector` and `querySelectorAll` are flexible and recommended for most cases.

---

## 2️⃣ Changing Content

```javascript
title.textContent = "Welcome!";
title.innerHTML = "<em>Welcome!</em>";
```

**Practical Example:** Updating live data

```javascript
const price = document.querySelector("#price");
let productPrice = 49.99;
price.textContent = `$${productPrice.toFixed(2)}`;
```

---

## 3️⃣ Changing Styles

```javascript
title.style.color = "red";
title.style.fontSize = "30px";
title.style.backgroundColor = "#f0f0f0";
```

**Example:** Toggle dark/light mode

```javascript
const body = document.body;
const toggleBtn = document.querySelector("#toggle-theme");

toggleBtn.addEventListener("click", () => {
  body.classList.toggle("dark-mode");
});
```

```css
/* CSS */
.dark-mode {
  background-color: #121212;
  color: #ffffff;
}
```

---

## 4️⃣ Creating & Removing Elements

### Create and append

```javascript
const list = document.querySelector("#list");
const newItem = document.createElement("li");
newItem.textContent = "New Task";
list.appendChild(newItem);
```

### Remove element

```javascript
const firstItem = document.querySelector("#list li");
firstItem.remove();
```

**Example:** To-do list add/remove

```javascript
const input = document.querySelector("#task-input");
const addBtn = document.querySelector("#add-task");

addBtn.addEventListener("click", () => {
  const li = document.createElement("li");
  li.textContent = input.value;
  list.appendChild(li);
  input.value = "";
});
```

---

## 5️⃣ Event Handling

### Click events

```javascript
const btn = document.querySelector("#btn-click");
btn.addEventListener("click", () => {
  alert("Button clicked!");
});
```

### Input / change events

```javascript
const nameInput = document.querySelector("#name");
nameInput.addEventListener("input", (e) => {
  console.log("Typed:", e.target.value);
});
```

### Event delegation

```javascript
document.querySelector("#list").addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    e.target.classList.toggle("completed");
  }
});
```

```css
.completed {
  text-decoration: line-through;
  opacity: 0.6;
}
```

---

## 6️⃣ Practical Applications

1. **Dynamic To-Do List** → add, remove, mark tasks complete
2. **Live Form Validation** → check input fields as the user types
3. **Theme Toggle** → switch between dark/light mode
4. **Interactive Product Page** → update price, availability, images
5. **Dynamic Modals / Popups** → show or hide content dynamically
6. **Tabs / Accordions** → display sections without page reload

---

## 📝 Exercises

1. Access the `<h1>` element and change its text to your name.
2. Change the color of all paragraphs to blue.
3. Create a new `<li>` item and append it to an existing `<ul>`.
4. Remove the first paragraph from the page.
5. Add a button that shows an alert when clicked.
6. Create a to-do list where you can add and remove tasks dynamically.
7. Implement a dark/light mode toggle using a button.
8. Update a paragraph text dynamically as the user types in an input field.
9. Make a list of products, each with a button to remove that product.
10. Create tabs where clicking a tab shows its content and hides others.

---

# 🎯 Summary

* The DOM lets JavaScript **interact with HTML and CSS**.
* Access elements using `getElementById`, `getElementsByClassName`, `querySelector`, or `querySelectorAll`.
* Change content using `textContent` or `innerHTML`.
* Change styles dynamically using `.style` or CSS classes.
* Create, append, and remove elements dynamically.
* Add event listeners for interactivity and efficiency.
* Practical applications include **interactive UI components, live updates, and dynamic apps**.

