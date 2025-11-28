# ⚡ JavaScript Events

Events allow JavaScript to **react to user actions** or **browser changes**.  
They are essential for creating **interactive web pages**.

Common event types include:

- **Mouse events** → click, mouseover, dblclick  
- **Keyboard events** → keydown, keyup, input  
- **Form events** → submit, change, focus, blur  
- **Window events** → load, resize, scroll  

---

## 1️⃣ Adding Event Listeners

The recommended way to handle events is using `addEventListener`.

```javascript
const button = document.querySelector("#myButton");

button.addEventListener("click", () => {
  alert("Button clicked!");
});
````

> Advantages of `addEventListener` over inline events: multiple listeners, cleaner separation of HTML and JS.

---

## 2️⃣ Mouse Events

| Event     | Description                       |
| --------- | --------------------------------- |
| click     | When an element is clicked        |
| dblclick  | When an element is double-clicked |
| mouseover | When mouse enters an element      |
| mouseout  | When mouse leaves an element      |
| mousedown | When mouse button is pressed      |
| mouseup   | When mouse button is released     |

```javascript
const box = document.querySelector("#box");

box.addEventListener("mouseover", () => {
  box.style.backgroundColor = "yellow";
});

box.addEventListener("mouseout", () => {
  box.style.backgroundColor = "lightblue";
});
```

---

## 3️⃣ Keyboard Events

| Event   | Description                        |
| ------- | ---------------------------------- |
| keydown | When a key is pressed              |
| keyup   | When a key is released             |
| input   | When the value of an input changes |

```javascript
const input = document.querySelector("#nameInput");

input.addEventListener("input", (e) => {
  console.log("User typed:", e.target.value);
});
```

---

## 4️⃣ Form Events

| Event  | Description                        |
| ------ | ---------------------------------- |
| submit | When a form is submitted           |
| change | When the value of an input changes |
| focus  | When an element receives focus     |
| blur   | When an element loses focus        |

```javascript
const form = document.querySelector("#myForm");

form.addEventListener("submit", (e) => {
  e.preventDefault(); // prevent page reload
  console.log("Form submitted!");
});
```

---

## 5️⃣ Window Events

| Event  | Description                    |
| ------ | ------------------------------ |
| load   | When the page finishes loading |
| resize | When the window is resized     |
| scroll | When the user scrolls          |

```javascript
window.addEventListener("resize", () => {
  console.log("Window resized:", window.innerWidth);
});
```

---

## 6️⃣ Event Delegation

Instead of attaching events to every element, attach one to a **parent** and detect the target:

```javascript
const list = document.querySelector("#list");

list.addEventListener("click", (e) => {
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

> Useful for **dynamic content** where elements are added later.

---

## 📝 Exercises

1. Add a click event to a button that changes the text of a paragraph.
2. Change the background color of a box when the mouse hovers over it.
3. Print each key typed in an input box to the console.
4. Prevent a form from submitting and log a message instead.
5. Make a list where clicking a list item toggles its “completed” style.
6. Log the window width whenever the user resizes the browser.

---

# 🎯 Summary

* Events let JavaScript **respond to user actions and browser changes**.
* Use `addEventListener` to attach events.
* Common event categories: **mouse, keyboard, form, window**.
* Event delegation improves efficiency for dynamic content.
* Practical applications: **interactive buttons, forms, to-do lists, real-time updates**.
