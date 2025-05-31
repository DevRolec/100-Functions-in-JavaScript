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
# 100 JavaScript Functions 
## 🔢 Math Functions (1–20)
```js
function add(a, b) { return a + b; }
function subtract(a, b) { return a - b; }
function multiply(a, b) { return a * b; }
function divide(a, b) { return b !== 0 ? a / b : null; }
function square(n) { return n * n; }
function cube(n) { return n * n * n; }
function power(base, exp) { return Math.pow(base, exp); }
function sqrt(n) { return Math.sqrt(n); }
function abs(n) { return Math.abs(n); }
function isEven(n) { return n % 2 === 0; }
function isOdd(n) { return n % 2 !== 0; }
function round(n) { return Math.round(n); }
function floor(n) { return Math.floor(n); }
function ceil(n) { return Math.ceil(n); }
function max(a, b) { return Math.max(a, b); }
function min(a, b) { return Math.min(a, b); }
function randomInt(min, max) { return Math.floor(Math.random() * (max - min + 1)) + min; }
function factorial(n) { return n <= 1 ? 1 : n * factorial(n - 1); }
function average(...nums) { return nums.reduce((a, b) => a + b, 0) / nums.length; }
function clamp(value, min, max) { return Math.max(min, Math.min(max, value)); }
```
