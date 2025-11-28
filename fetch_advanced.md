# 🌐 Fetch API Advanced Topics in JavaScript

The **Fetch API** is a modern way to make HTTP requests in JavaScript.  
Advanced techniques allow you to **handle multiple requests, errors, and optimize data fetching** in real-world applications.

---

## 1️⃣ Basic Fetch Refresher

```javascript
fetch("https://jsonplaceholder.typicode.com/posts/1")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Error:", error));
````

* `fetch(url)` returns a **Promise**
* `.json()` converts response to a JavaScript object
* `.catch()` handles network errors

---

## 2️⃣ Handling Multiple Requests with `Promise.all`

```javascript
const urls = [
  "https://jsonplaceholder.typicode.com/posts/1",
  "https://jsonplaceholder.typicode.com/posts/2",
  "https://jsonplaceholder.typicode.com/posts/3"
];

Promise.all(urls.map(url => fetch(url).then(res => res.json())))
  .then(results => {
    results.forEach(post => console.log(post.title));
  })
  .catch(error => console.error("One of the requests failed:", error));
```

* `Promise.all()` waits for **all promises** to resolve
* Ideal for fetching **multiple API endpoints simultaneously**

---

## 3️⃣ Using `async/await` with Fetch

```javascript
async function getPosts() {
  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts");
    if (!response.ok) {
      throw new Error("Network response was not ok");
    }
    const posts = await response.json();
    posts.slice(0, 5).forEach(post => console.log(post.title));
  } catch (error) {
    console.error("Fetch error:", error);
  }
}

getPosts();
```

* `async/await` makes asynchronous code **more readable**
* Always check `response.ok` to handle **HTTP errors**

---

## 4️⃣ POST Requests (Sending Data)

```javascript
async function addPost() {
  const newPost = {
    title: "New Post",
    body: "This is a test post",
    userId: 1
  };

  try {
    const response = await fetch("https://jsonplaceholder.typicode.com/posts", {
      method: "POST",
      headers: {
        "Content-Type": "application/json"
      },
      body: JSON.stringify(newPost)
    });

    const data = await response.json();
    console.log("Created Post:", data);
  } catch (error) {
    console.error("Error creating post:", error);
  }
}

addPost();
```

* Use `method: "POST"` and `body: JSON.stringify(data)` to send data
* Include proper `Content-Type` headers

---

## 5️⃣ Advanced Error Handling

```javascript
async function safeFetch(url) {
  try {
    const response = await fetch(url);
    if (!response.ok) throw new Error(`HTTP error! Status: ${response.status}`);
    const data = await response.json();
    return data;
  } catch (error) {
    console.error("Fetch failed:", error);
    return null; // Return a default value or handle gracefully
  }
}
```

* Always **check HTTP status**
* Use `try/catch` to prevent your app from crashing

---

## 6️⃣ Practical Tips

* Use `Promise.all()` for **parallel requests**
* Always handle **network and HTTP errors**
* Prefer **async/await** for readability in complex logic
* For APIs that support it, consider **pagination** and **lazy loading**
* Combine with **Template Rendering / Dynamic HTML** for interactive UI

---

## 📝 Exercises

1. Fetch 3 posts from the API and log their titles using `Promise.all`.
2. Write an async function to fetch users and render their names in a list.
3. Create a form that sends a POST request to create a new user.
4. Implement error handling for a fetch request to a wrong URL.
5. Fetch posts in pages (e.g., 5 posts at a time) and render them dynamically.

---

# 🎯 Summary

* Fetch API is **modern, promise-based, and flexible**.
* Combine **async/await** with proper error handling for cleaner code.
* `Promise.all()` allows **parallel API calls**.
* Handle **POST, PUT, DELETE** requests as needed.
* Essential for **real-world web applications that interact with APIs**.

