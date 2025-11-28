# 🏛️ Classes & Object-Oriented JavaScript (OOP)

JavaScript supports **Object-Oriented Programming (OOP)** — a programming paradigm that organizes code into **objects** that contain both **data** (properties) and **behaviors** (methods).

ES6 introduced the **class** syntax to make object-oriented programming easier and cleaner.

---

## 1️⃣ What Are Classes?

A **class** is a blueprint for creating objects.

Think of a class as a template, and objects as copies built from that template.

Example:

```javascript
class Person {
  constructor(name, age) {
    this.name = name;
    this.age = age;
  }
}
````

Nothing happens until you create an **object** from the class:

```javascript
const person1 = new Person("John", 25);
console.log(person1);
```

---

## 2️⃣ The `constructor` Method

Every class can have a **constructor**, which runs automatically when creating an object.

```javascript
class Car {
  constructor(model, year) {
    this.model = model;
    this.year = year;
  }
}

const car1 = new Car("Toyota", 2020);
```

The constructor:

* Sets initial values
* Prepares the object

---

## 3️⃣ Adding Methods

Methods are functions inside a class.

```javascript
class Car {
  constructor(model, year) {
    this.model = model;
    this.year = year;
  }

  start() {
    console.log(`${this.model} is starting...`);
  }
}

const car = new Car("Honda", 2022);
car.start();
```

---

## 4️⃣ Inheritance — `extends` & `super()`

One class can **inherit** from another, allowing reuse of functionality.

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }

  speak() {
    console.log(`${this.name} makes a sound`);
  }
}

class Dog extends Animal {
  constructor(name, breed) {
    super(name); // call parent constructor
    this.breed = breed;
  }

  bark() {
    console.log(`${this.name} barks loudly!`);
  }
}

const dog = new Dog("Rex", "German Shepherd");
dog.speak();
dog.bark();
```

Inheritance allows:

* Reusing logic
* Extending behavior
* Organizing code better

---

## 5️⃣ Getters and Setters

Useful for controlling how properties are accessed or modified.

```javascript
class User {
  constructor(username) {
    this._username = username;
  }

  get username() {
    return this._username.toUpperCase();
  }

  set username(value) {
    this._username = value.trim();
  }
}

const user = new User("abideen");
console.log(user.username);  // ABIDEEN
```

---

## 6️⃣ Static Methods

Static methods belong to the **class itself**, not the objects.

```javascript
class MathTools {
  static add(a, b) {
    return a + b;
  }
}

console.log(MathTools.add(3, 5)); // 8
```

Use static methods for utilities or helper functions.

---

## 7️⃣ Practical Real-Life Uses

Classes are perfect for:

* Modeling real-world entities (Users, Cars, Products)
* Games (Players, Enemies, Weapons)
* Apps (Tasks, Items, Components)
* API data models (Post, Comment, Order)
* DOM UI components (Modals, Sliders, Forms)

---

## 🧪 Mini Exercises

1. Create a `Student` class with `name`, `level`, and a `study()` method.
2. Create a `Rectangle` class with a method to calculate area.
3. Create a `BankAccount` class with `deposit()` and `withdraw()` methods.
4. Create a `Phone` class and extend it with a `Smartphone` class.
5. Make a class with a getter and setter for `email`.

---

## 🎯 Summary

* Classes are templates for creating objects.
* The `constructor()` method initializes new object instances.
* Methods define behaviors.
* `extends` and `super()` enable inheritance.
* Getters and setters control property access.
* Static methods belong to the class, not the object.

Classes help you write **clean, structured, and scalable** JavaScript.

