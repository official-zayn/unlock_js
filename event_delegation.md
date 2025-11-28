# 🧩 Event Delegation & Advanced Event Handling

Event delegation is a powerful JavaScript technique that allows you to **handle events efficiently**, especially when working with dynamic or frequently changing DOM elements.

Instead of attaching event listeners to multiple child elements, you attach **one listener to a parent element** and detect which child triggered the event.

---

## 🔍 Why Event Delegation?

### Without delegation:
- You add listeners to many individual elements.
- Inefficient and harder to maintain.
- Fails for elements added later (dynamic elements).

### With event delegation:
- One listener handles all children.
- Works for dynamically added elements.
- More efficient and scalable.

---

## 1️⃣ Basic Example — Event Delegation

Instead of adding a click event to each button:

```javascript
document.getElementById("list").addEventListener("click", function (e) {
  if (e.target && e.target.matches(".item")) {
    console.log("Clicked:", e.target.textContent);
  }
});
````

```html
<ul id="list">
  <li class="item">Item 1</li>
  <li class="item">Item 2</li>
  <li class="item">Item 3</li>
</ul>
```

### ✔ What happens:

* The `ul` listens for all clicks.
* `e.target` tells which `li` was clicked.
* New items added later will also work.

---

## 2️⃣ Matching Targets with `matches()`

```javascript
if (e.target.matches(".btn-delete")) {
  console.log("Delete button clicked");
}
```

`matches()` lets you check if the clicked element fits a selector.

---

## 3️⃣ Stopping Event Bubbling

Sometimes child elements trigger unwanted parent events.

Use:

```javascript
e.stopPropagation();
```

Example:

```javascript
button.addEventListener("click", function (e) {
  e.stopPropagation();
  console.log("Button clicked only");
});
```

---

## 4️⃣ Preventing Default Behavior

Use `preventDefault()` to stop default browser actions:

```javascript
link.addEventListener("click", function (e) {
  e.preventDefault();
  console.log("Link click prevented");
});
```

---

## 5️⃣ Delegation with Dynamic Elements

Perfect for todo lists, messages, notifications, etc.

```javascript
document.querySelector(".todos").addEventListener("click", (e) => {
  if (e.target.classList.contains("delete")) {
    e.target.parentElement.remove();
  }
});
```

Dynamically adding items:

```javascript
document.querySelector("#add").addEventListener("click", () => {
  const li = document.createElement("li");
  li.innerHTML = "New Item <button class='delete'>X</button>";
  document.querySelector(".todos").appendChild(li);
});
```

No extra listeners needed.

---

## 6️⃣ Capturing vs Bubbling (Advanced)

By default, events propagate **upwards** (bubbling).
You can switch to **capturing** mode:

```javascript
element.addEventListener("click", handler, true);
```

* `true` → capture phase
* `false` → bubble phase (default)

---

## 🧠 When to Use Event Delegation

Use delegation when:

* You have **many similar elements** (list items, buttons).
* Elements are **added dynamically**.
* Performance and memory efficiency matter.

Avoid delegation when:

* You need very specific element behavior.
* Event should *not* bubble (rare cases).

---

## 📝 Practice Exercise

### Exercise 1:

Create a list of items. When any item is clicked, highlight it using delegation.

### Exercise 2:

Build a dynamic todo list where delete buttons work using only **one event listener**.

### Exercise 3:

Use `stopPropagation()` to prevent inner buttons from triggering outer elements.

---

# ✅ Summary

Event delegation allows you to:

* Handle events efficiently
* Reduce the number of event listeners
* Manage dynamic elements easily
* Control event bubbling and capturing
* Improve code performance and structure

It is one of the most **essential techniques** for real-world web apps.
