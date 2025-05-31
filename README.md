# 100-Functions-in-JavaScript
## A function in JavaScript is a reusable block of code that performs a specific task. You can call a function whenever you need it, which helps avoid repeating code.
---
🧠 Basic Concept
Think of a function like a machine:

You give it input (called parameters or arguments).

It does something (logic or computation).

It returns output (or just performs an action).
---

In JavaScript, there are several types of functions, each serving different purposes or written in different ways. Here's a clear breakdown:

1. Named Function (Function Declaration)
A standard function with a name.

```js
function greet() {
  console.log("Hello!");
}
✅ Hoisted – you can call it before it’s defined.
```
2. Anonymous Function (Function Expression)
A function without a name, assigned to a variable.

```js
const sayHello = function() {
  console.log("Hello!");
};
```
🚫 Not hoisted – must be defined before calling.

3. Arrow Function (ES6+)
A shorter way to write functions. Best for simple tasks.

```js
const add = (a, b) => a + b;
```
⚠️ Doesn’t have its own this, so avoid for object methods or constructors.

4. Immediately Invoked Function Expression (IIFE)
A function that runs immediately after it’s defined.

```js
(function() {
  console.log("I run instantly!");
})();
```
Useful for creating a private scope.

5. Constructor Function
Used with the new keyword to create objects.

```js
function Person(name) {
  this.name = name;
}
```
const user = new Person("Ada");
✅ Can define properties and methods using this.

6. Generator Function
Returns an iterator and can pause/resume using yield.

```js
function* count() {
  yield 1;
  yield 2;
  yield 3;
}

const counter = count();
console.log(counter.next().value); // 1
```
7. Callback Function
Passed as an argument to another function.

```js
function process(callback) {
  callback();
}

process(() => console.log("Callback executed"));
```
Widely used in async code (like setTimeout, fetch, etc.).

8. Async Function (ES8+)
Handles asynchronous operations using async/await.
```js
async function fetchData() {
  const res = await fetch("https://api.example.com");
  const data = await res.json();
  console.log(data);
}
```
