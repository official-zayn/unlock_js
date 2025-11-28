# 🧩 Template Rendering / Dynamic HTML with JavaScript

Creating HTML dynamically using JavaScript is essential for **building interactive, data-driven web applications**.  
This technique allows you to **render content from arrays, objects, or APIs directly into the DOM**.

---

## 1️⃣ Simple Dynamic Rendering

```javascript
const container = document.getElementById("container");

const items = ["Apple", "Banana", "Cherry"];

items.forEach(item => {
  const p = document.createElement("p");
  p.textContent = item;
  container.appendChild(p);
});
````

* `document.createElement()` → create new HTML elements
* `textContent` → set text
* `appendChild()` → add element to the DOM

---

## 2️⃣ Using Template Literals

Template literals make it **easier to render complex HTML**:

```javascript
const products = [
  { name: "Laptop", price: 1200 },
  { name: "Phone", price: 700 }
];

const container = document.getElementById("container");

products.forEach(product => {
  container.innerHTML += `
    <div class="product-card">
      <h2>${product.name}</h2>
      <p>Price: $${product.price}</p>
    </div>
  `;
});
```

* `${}` → insert JavaScript values inside HTML
* Useful for **repeating structures like cards, lists, or tables**

---

## 3️⃣ Rendering from API (Fetch + Templates)

```javascript
const container = document.getElementById("container");

async function getUsers() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/users");
    const users = await response.json();
    
    users.forEach(user => {
      container.innerHTML += `
        <div class="user-card">
          <h3>${user.name}</h3>
          <p>Email: ${user.email}</p>
        </div>
      `;
    });
  } catch (error) {
    console.error("Error fetching users:", error);
  }
}

getUsers();
```

* Combine **fetch, JSON, and template literals** for dynamic content
* Ideal for **blogs, dashboards, and user lists**

---

## 4️⃣ Using `map()` for Rendering

```javascript
const fruits = ["Apple", "Banana", "Cherry"];

const html = fruits.map(fruit => `<li>${fruit}</li>`).join("");
document.getElementById("fruit-list").innerHTML = html;
```

* `map()` transforms arrays into HTML strings
* `join("")` combines array into a single string

---

## 5️⃣ Practical Applications

* Product catalogs or e-commerce pages
* User dashboards or profile lists
* Dynamic tables or cards from API data
* Rendering quiz questions or interactive forms

---

## 📝 Exercises

1. Create an array of 5 movies and display their names and release year in cards.
2. Fetch posts from `https://jsonplaceholder.typicode.com/posts` and render the first 5 titles dynamically.
3. Render a table of students with their name and grade from an array of objects.
4. Use `map()` to generate a list of links from an array of URLs.
5. Update a section dynamically when a button is clicked, replacing the content.

---

# 🎯 Summary

* Use **`createElement`** or **template literals** to render HTML dynamically.
* Combine **arrays, objects, and API data** for interactive content.
* `map()` and `.forEach()` are great tools for rendering repeated elements.
* Dynamic HTML is **essential for modern, interactive web applications**.

