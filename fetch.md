# 🌐 Fetch API & JSON in JavaScript

The **Fetch API** allows you to request data from a server, and **JSON (JavaScript Object Notation)** is the most common format for sending data.  

Together, they enable **dynamic web applications** that fetch and display data without reloading the page.

---

## 1️⃣ Basic Fetch

```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then(response => response.json()) // parse JSON
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
````

* `fetch(url)` → starts the request
* `.then(response => response.json())` → converts the response to a JS object
* `.catch()` → handles errors

---

## 2️⃣ Fetch with Async/Await

```javascript
async function getPost() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts/1");
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Error:", error);
  }
}

getPost();
```

* `async` → marks the function as asynchronous
* `await` → waits for the fetch or JSON parsing to complete

---

## 3️⃣ Fetching Multiple Items

```javascript
async function getPosts() {
  const response = await fetch("https://jsonplaceholder.typicode.com/posts");
  const posts = await response.json();
  posts.forEach(post => console.log(post.title));
}

getPosts();
```

* Fetches an array of posts and loops through them.
* You can display these dynamically in the DOM.

---

## 4️⃣ Sending Data (POST Request)

```javascript
async function createPost() {
  const response = await fetch("https://jsonplaceholder.typicode.com/posts", {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify({
      title: "My New Post",
      body: "This is the post content",
      userId: 1
    })
  });

  const data = await response.json();
  console.log(data);
}

createPost();
```

* `method: "POST"` → send data to the server
* `body: JSON.stringify(obj)` → convert JS object to JSON string
* `headers` → tell the server that we’re sending JSON

---

## 5️⃣ Practical Applications

* Load data dynamically for a **blog, news, or product page**
* Submit **forms without page reload**
* Fetch **user information from APIs**
* Display **dynamic content in tables, cards, or lists**

---

## 📝 Exercises

1. Fetch a single post from `https://jsonplaceholder.typicode.com/posts/1` and log the title.
2. Fetch all posts and display the first 5 titles in the console.
3. Create a function to add a new post using a POST request.
4. Handle errors when the fetch fails.
5. Display fetched data dynamically in the HTML page using DOM manipulation.

---

# 🎯 Summary

* **Fetch API** requests data from servers.
* **JSON** is the standard format for sending and receiving data.
* Use `.then()` or `async/await` to handle asynchronous fetch calls.
* Can perform **GET** and **POST** requests.
* Combine with **DOM manipulation** to create dynamic, interactive web pages.
