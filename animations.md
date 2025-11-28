# 🎨 Animations & CSS Interaction with JavaScript

JavaScript can **interact with CSS** to create animations and dynamic effects, making web pages more **interactive and engaging**.

---

## 1️⃣ Changing Styles Dynamically

```javascript
const box = document.getElementById("box");

box.style.backgroundColor = "blue";
box.style.width = "200px";
box.style.height = "200px";
````

* Use `.style.property` to **manipulate CSS properties** directly.
* Useful for **hover effects, toggles, or visual feedback**.

---

## 2️⃣ Adding and Removing Classes

```javascript
const box = document.getElementById("box");

box.classList.add("active");   // Add class
box.classList.remove("active"); // Remove class
box.classList.toggle("active"); // Toggle class
```

* Manage **predefined CSS animations** via classes for cleaner code.

```css
/* Example CSS */
.active {
  transform: scale(1.2);
  transition: transform 0.3s ease;
}
```

---

## 3️⃣ CSS Transitions with JS

* Smooth changes over time using `transition`:

```javascript
const box = document.getElementById("box");

box.addEventListener("click", () => {
  box.style.transform = "rotate(45deg)";
  box.style.transition = "transform 0.5s ease";
});
```

* Transitions make **state changes smooth** instead of abrupt.

---

## 4️⃣ Using `requestAnimationFrame` for Animations

```javascript
const box = document.getElementById("box");
let position = 0;

function animate() {
  position += 2;
  box.style.left = position + "px";

  if (position < 300) {
    requestAnimationFrame(animate);
  }
}

animate();
```

* `requestAnimationFrame()` is **efficient** and synced with browser rendering.
* Preferred for **smooth animations over setInterval**.

---

## 5️⃣ Keyframe Animations via JS

* Dynamically trigger CSS animations:

```css
/* CSS */
@keyframes slide {
  from { transform: translateX(0); }
  to { transform: translateX(300px); }
}

.slide {
  animation: slide 2s forwards;
}
```

```javascript
const box = document.getElementById("box");
box.classList.add("slide");
```

* Combine JS **events** with CSS **keyframes** for interactive animations.

---

## 6️⃣ Practical Applications

* Interactive **sliders or carousels**
* Hover effects and **button animations**
* Loading indicators or **spinners**
* Animating charts or dashboards

---

## 📝 Exercises

1. Create a box that changes color on click using JS.
2. Toggle a class that applies a scale animation on hover.
3. Animate a box moving across the screen using `requestAnimationFrame`.
4. Combine keyframes and JS to create a sliding notification.
5. Create a bouncing ball animation using CSS keyframes triggered by JS.

---

# 🎯 Summary

* JavaScript can **manipulate styles and classes** to create dynamic effects.
* `requestAnimationFrame()` allows **smooth, efficient animations**.
* Combine **CSS transitions and keyframes** with JS for interactive UI.
* Essential for **enhancing user experience and modern web design**.


