# 🚀 JavaScript Functions Masterclass

Welcome to the ultimate guide to **JavaScript Functions** — from beginner basics to advanced mastery. This course is project-based, example-driven, and designed to build your skills step by step.

> 🔥 No frameworks. No fluff. Just pure JavaScript functions mastery.

---

## 📚 Course Structure

Each section is a folder with lessons and exercises.

### 🟢 1. Beginner (Function Basics)
- What is a function?
- Function declarations vs expressions
- Parameters and arguments
- Return values
- Function scope

### 🟡 2. Intermediate (Function Mechanics)
- Arrow functions
- Default parameters
- Rest and spread with functions
- Callback functions
- Higher-order functions
- Function expressions vs declarations

### 🔴 3. Advanced (Function Power)
- Closures
- IIFE (Immediately Invoked Function Expressions)
- Recursion
- The `this` keyword inside functions
- Binding: `.call()`, `.apply()`, `.bind()`
- Currying and partial application
- Pure functions and side effects

---

## 🧠 Projects & Challenges
Each level includes:
- 📄 `lesson.md` → Theory & explanation
- 📁 `examples/` → Code examples
- 🧪 `exercises/` → Practice problems
- ✅ `solutions/` → Completed answers

---

## 🚦 Getting Started


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
## 🔤 String Functions (21–40)
```js
function capitalize(str) { return str.charAt(0).toUpperCase() + str.slice(1); }
function reverseString(str) { return str.split('').reverse().join(''); }
function isPalindrome(str) { return str === reverseString(str); }
function truncate(str, len) { return str.length > len ? str.slice(0, len) + '...' : str; }
function toCamelCase(str) { return str.replace(/[-_](.)/g, (_, c) => c.toUpperCase()); }
function toKebabCase(str) { return str.replace(/\s+/g, '-').toLowerCase(); }
function toSnakeCase(str) { return str.replace(/\s+/g, '_').toLowerCase(); }
function countVowels(str) { return (str.match(/[aeiou]/gi) || []).length; }
function removeSpaces(str) { return str.replace(/\s/g, ''); }
function repeatString(str, times) { return str.repeat(times); }
function startsWith(str, prefix) { return str.startsWith(prefix); }
function endsWith(str, suffix) { return str.endsWith(suffix); }
function includesStr(str, val) { return str.includes(val); }
function getInitials(name) { return name.split(' ').map(n => n[0]).join(''); }
function escapeHTML(str) { return str.replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;"); }
function unescapeHTML(str) { return str.replace(/&lt;/g, "<").replace(/&gt;/g, ">").replace(/&amp;/g, "&"); }
function isUpperCase(str) { return str === str.toUpperCase(); }
function isLowerCase(str) { return str === str.toLowerCase(); }
function stripTags(str) { return str.replace(/<[^>]*>?/gm, ''); }
function countWords(str) { return str.trim().split(/\s+/).length; }
```
##  📦 Array Functions (41–60)
```js
function sumArray(arr) { return arr.reduce((a, b) => a + b, 0); }
function maxInArray(arr) { return Math.max(...arr); }
function minInArray(arr) { return Math.min(...arr); }
function removeDuplicates(arr) { return [...new Set(arr)]; }
function flattenArray(arr) { return arr.flat(Infinity); }
function chunkArray(arr, size) { return Array.from({ length: Math.ceil(arr.length / size) }, (_, i) => arr.slice(i * size, i * size + size)); }
function arrayDifference(a, b) { return a.filter(i => !b.includes(i)); }
function arrayIntersection(a, b) { return a.filter(i => b.includes(i)); }
function shuffleArray(arr) { return arr.sort(() => Math.random() - 0.5); }
function lastElement(arr) { return arr[arr.length - 1]; }
function firstElement(arr) { return arr[0]; }
function isArrayEmpty(arr) { return arr.length === 0; }
function mergeArrays(a, b) { return [...a, ...b]; }
function sortArrayAsc(arr) { return [...arr].sort((a, b) => a - b); }
function sortArrayDesc(arr) { return [...arr].sort((a, b) => b - a); }
function findDuplicates(arr) { return arr.filter((item, index) => arr.indexOf(item) !== index); }
function uniqueByKey(arr, key) { return [...new Map(arr.map(obj => [obj[key], obj])).values()]; }
function arrayToObject(arr) { return Object.assign({}, arr); }
function objectToArray(obj) { return Object.entries(obj); }
function countOccurrences(arr, val) { return arr.filter(x => x === val).length; }
```
## 🕒 Date & Time Functions (61–75)
```js
function getCurrentDate() { return new Date(); }
function formatDate(date) { return date.toISOString().split('T')[0]; }
function getYear(date) { return date.getFullYear(); }
function getMonth(date) { return date.getMonth() + 1; }
function getDay(date) { return date.getDate(); }
function addDays(date, days) { let d = new Date(date); d.setDate(d.getDate() + days); return d; }
function subtractDays(date, days) { let d = new Date(date); d.setDate(d.getDate() - days); return d; }
function daysBetween(d1, d2) { return Math.ceil(Math.abs((d1 - d2) / (1000 * 60 * 60 * 24))); }
function isWeekend(date) { return [0, 6].includes(date.getDay()); }
function getDayName(date) { return date.toLocaleDateString('en-US', { weekday: 'long' }); }
function getMonthName(date) { return date.toLocaleDateString('en-US', { month: 'long' }); }
function isLeapYear(year) { return (year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0); }
function timeSince(date) { return Math.floor((new Date() - date) / 1000); }
function isToday(date) { const d = new Date(); return date.toDateString() === d.toDateString(); }
function isPast(date) { return new Date() > date; }
```
🧱 Object & Utility Functions (76–85)
```js
function deepClone(obj) { return JSON.parse(JSON.stringify(obj)); }
function isObject(val) { return val && typeof val === 'object' && !Array.isArray(val); }
function isEmptyObject(obj) { return Object.keys(obj).length === 0; }
function mergeObjects(a, b) { return { ...a, ...b }; }
function objectHasKey(obj, key) { return obj.hasOwnProperty(key); }
function getType(val) { return Object.prototype.toString.call(val).slice(8, -1); }
function debounce(fn, delay) { let timer; return (...args) => { clearTimeout(timer); timer = setTimeout(() => fn(...args), delay); }; }
function throttle(fn, limit) { let lastCall = 0; return (...args) => { const now = Date.now(); if (now - lastCall >= limit) { lastCall = now; fn(...args); } }; }
function generateUUID() { return crypto.randomUUID(); }
function parseJSON(str) { try { return JSON.parse(str); } catch { return null; } }
```
🧪 Type Checking (86–90)
```js
function isNumber(val) { return typeof val === 'number'; }
function isString(val) { return typeof val === 'string'; }
function isBoolean(val) { return typeof val === 'boolean'; }
function isFunction(val) { return typeof val === 'function'; }
function isArray(val) { return Array.isArray(val); }
```
🌐 DOM & Browser Utilities (91–100)
```js

function getById(id) { return document.getElementById(id); }
function getByClass(cls) { return document.getElementsByClassName(cls); }
function getByTag(tag) { return document.getElementsByTagName(tag); }
function query(selector) { return document.querySelector(selector); }
function queryAll(selector) { return document.querySelectorAll(selector); }
function setText(id, text) { const el = getById(id); if (el) el.textContent = text; }
function setHTML(id, html) { const el = getById(id); if (el) el.innerHTML = html; }
function addClass(id, className) { const el = getById(id); if (el) el.classList.add(className); }
function removeClass(id, className) { const el = getById(id); if (el) el.classList.remove(className); }
function toggleClass(id, className) { const el = getById(id); if (el) el.classList.toggle(className); }
```
## Basic JS Functions

Function to roll a die
```js
function rollDie() {
  return Math.floor(Math.random() * 6) + 1;
}
```
🚀 1. Number Adder App
🧠 Concepts: DOM, event handling, basic arithmetic
What it does: Takes two numbers from input fields and displays their sum when a button is clicked.
```js
function addNumbers(a, b) {
  return a + b;
}
```
🎲 2. Dice Roller
🧠 Concepts: Random numbers, functions, DOM
What it does: Simulates rolling a 6-sided die and shows the result.
```js
function rollDice() {
    const diceFaces = ["⚀", "⚁", "⚂", "⚃", "⚄", "⚅"];
    const roll1 = Math.floor(Math.random() * 6);
    const roll2 = Math.floor(Math.random() * 6);

    document.getElementById("dice1").textContent = diceFaces[roll1];
    document.getElementById("dice2").textContent = diceFaces[roll2];

    if (roll1 > roll2) {
        document.getElementById("resultDice").textContent = "🎉  Player 1 wins!";
    } else if (roll1 < roll2) {
        document.getElementById("resultDice").textContent = "🎉  Player 2 wins!";
    } else {
        document.getElementById("resultDice").textContent = "🤝 It's a tie!";  
    }   
}
```
3. Rock Paper and Scissors Game
  🧠 Concepts: Random numbers, functions, DOM
What it does: Simulates a game experience of making choices between Rock Paper and Scissors. where set rules are implemented
```js

const playerScoreSpan = document.getElementById("player-score");
const cpuScoreSpan = document.getElementById("cpu-score");
const playerChoiceSpan = document.getElementById("player-choice");
const cpuChoiceSpan = document.getElementById("cpu-choice");
const resultMessage = document.getElementById("result-message");

const winSound = document.getElementById("win-sound");
const loseSound = document.getElementById("lose-sound");
const drawSound = document.getElementById("draw-sound");

let playerScore = 0;
let cpuScore = 0;

const choices = ["rock", "paper", "scissors"];

document.querySelectorAll(".choice").forEach(button => {
  button.addEventListener("click", () => {
    const playerChoice = button.dataset.choice;
    playerChoiceSpan.textContent = playerChoice;

    // CPU "thinking" animation
    cpuChoiceSpan.textContent = "...";
    resultMessage.textContent = "CPU is thinking...";

    setTimeout(() => {
      const cpuChoice = getCpuChoice();
      cpuChoiceSpan.textContent = cpuChoice;

      const result = getWinner(playerChoice, cpuChoice);
      updateScores(result);
      showResultMessage(result);
    }, 600);
  });
});

function getCpuChoice() {
  const randIndex = Math.floor(Math.random() * choices.length);
  return choices[randIndex];
}

function getWinner(player, cpu) {
  if (player === cpu) return "draw";
  if (
    (player === "rock" && cpu === "scissors") ||
    (player === "paper" && cpu === "rock") ||
    (player === "scissors" && cpu === "paper")
  ) {
    return "win";
  }
  return "lose";
}

function updateScores(result) {
  if (result === "win") {
    playerScore++;
    playerScoreSpan.textContent = playerScore;
    winSound.play();
  } else if (result === "lose") {
    cpuScore++;
    cpuScoreSpan.textContent = cpuScore;
    loseSound.play();
  } else {
    drawSound.play();
  }
}

function showResultMessage(result) {
  if (result === "win") {
    resultMessage.textContent = "🎉 You Win!";
    resultMessage.style.color = "#00ff88";
  } else if (result === "lose") {
    resultMessage.textContent = "💀 You Lose!";
    resultMessage.style.color = "#ff4444";
  } else {
    resultMessage.textContent = "🤝 It's a Draw!";
    resultMessage.style.color = "#cccccc";
  }
}

```
---

## 1. Beginner: Function Basics

### 🧠 What is a Function?

A function is a reusable block of code that performs a specific task.

### 🔧 Function Declaration

```js
function greet() {
  console.log("Hello!");
}
```

Call it with:

```js
greet();
```

### 🧩 Parameters and Arguments

```js
function greet(name) {
  console.log("Hello, " + name + "!");
}

greet("Alice"); // Hello, Alice!
```

### 🔁 Return Values

```js
function add(a, b) {
  return a + b;
}

let sum = add(3, 4); // 7
```

### 🏠 Function Scope

Variables declared inside a function cannot be accessed outside.

```js
function showScope() {
  let secret = "hidden";
  console.log(secret);
}

// console.log(secret); // Error
```

### ✅ Beginner Examples

```js
function sayHi() {
  console.log("Hi there!");
}

function multiply(a, b) {
  return a * b;
}

function isEven(num) {
  return num % 2 === 0;
}
```

### 💪 Beginner Exercises

1. Write a function that subtracts two numbers.
2. Write a function that returns "even" or "odd" based on an input number.
3. Create a function that converts Celsius to Fahrenheit.
4. Create a function that returns the square of a number.

### 🧠 Beginner Solutions

```js
function subtract(a, b) {
  return a - b;
}

function evenOrOdd(n) {
  return n % 2 === 0 ? "even" : "odd";
}

function celsiusToFahrenheit(c) {
  return (c * 9) / 5 + 32;
}

function square(n) {
  return n * n;
}
```

---

## 2. Intermediate: Function Mechanics

### ➡️ Arrow Functions

```js
const greet = (name) => {
  console.log("Hello, " + name);
};
```

Short version:

```js
const add = (a, b) => a + b;
```

### 🛠 Default Parameters

```js
function greet(name = "Stranger") {
  console.log("Hello, " + name);
}
```
## 🏹 JavaScript Arrow Functions Tutorial
### 📌 What Are Arrow Functions?
Arrow functions are a shorter syntax for writing functions in JavaScript, introduced in ES6 (ECMAScript 2015).
They are commonly used in modern JavaScript code because they are concise and work especially well with callbacks and array methods.

✅ Basic Syntax
```js
// Traditional Function
function add(a, b) {
  return a + b;
}

// Arrow Function
const add = (a, b) => a + b;
```
🔄 Syntax Variations
Use Case	Syntax	Example
No parameters	() => {}	() => console.log("Hello")
One parameter	param => {}	name => console.log(name)
Multiple parameters	(a, b) => {}	(x, y) => x * y
One line return	() => value	(a, b) => a + b
With block body	() => { return ... }	(a, b) => { return a + b; }

⚠️ Important Notes
1. No this Binding
Arrow functions do not have their own this. They inherit this from the enclosing scope.

```js
function Counter() {
  this.count = 0;
  setInterval(() => {
    this.count++;
    console.log(this.count);
  }, 1000);
}
```
new Counter(); // Works as expected
2. Cannot be used as constructors
You cannot use arrow functions with new keyword.

```js
const Person = (name) => {
  this.name = name;
};
// ❌ new Person('John'); // Error!
```
3. No arguments Object
Arrow functions do not have their own arguments object.

🔁 Practice Examples
Example 1: Add Two Numbers
```js
const add = (a, b) => a + b;
console.log(add(3, 5)); // 8
```
Example 2: Square a Number
```js
const square = n => n * n;
console.log(square(4)); // 16
Example 3: Use with .map()

const nums = [1, 2, 3];
const doubled = nums.map(n => n * 2);
console.log(doubled); // [2, 4, 6]
```
Example 4: Filtering with .filter()
```js
const ages = [12, 17, 19, 24];
const adults = ages.filter(age => age >= 18);
console.log(adults); // [19, 24]
```
🎯 Practice Tasks
Try these on your own:

Create an arrow function to check if a number is even.

Use an arrow function inside forEach to print each item in an array.

Write an arrow function to return the length of a string.


---
### 📦 Rest Parameters

```js
function sum(...nums) {
  return nums.reduce((a, b) => a + b, 0);
}
```

### 📤 Spread with Functions

```js
const numbers = [1, 2, 3];
console.log(Math.max(...numbers)); // 3
```

### 📞 Callback Functions

```js
function processUserInput(callback) {
  const name = "Alice";
  callback(name);
}
```

### 🔁 Higher-Order Functions

```js
function multiplier(factor) {
  return function (number) {
    return number * factor;
  };
}
```

### ✅ Intermediate Examples

```js
const greet = name => console.log(`Hi, ${name}`);

const average = (...nums) => nums.reduce((a, b) => a + b) / nums.length;

function repeatTask(n, task) {
  for (let i = 0; i < n; i++) {
    task();
  }
}
```

### 💪 Intermediate Exercises

1. Create a function that returns the maximum number from any amount of arguments.
2. Create a higher-order function that accepts a function and a number and calls the function that many times.
3. Write a function that accepts another function and returns a new function that adds 1 to the result.

### 🧠 Intermediate Solutions

```js
function maxOf(...nums) {
  return Math.max(...nums);
}

function repeat(n, fn) {
  for (let i = 0; i < n; i++) {
    fn();
  }
}

function plusOneDecorator(fn) {
  return function (...args) {
    return fn(...args) + 1;
  };
}
```

---

## 3. Advanced: Function Power

### 🔄 Closures

```js
function outer() {
  let count = 0;
  return function () {
    count++;
    return count;
  };
}
```

### ⚡ IIFE (Invoked Function Expression )

```js
(function () {
  console.log("This runs immediately");
})();
```

### 🔁 Recursion

```js
function factorial(n) {
  if (n === 0) return 1;
  return n * factorial(n - 1);
}
```

### 🔍 The `this` Keyword

```js
const person = {
  name: "Alice",
  greet() {
    console.log("Hello, I am " + this.name);
  }
};
```

### 🔗 `bind`, `call`, and `apply`

```js
function sayHi() {
  console.log("Hi " + this.name);
}

const user = { name: "Bob" };
sayHi.call(user);
sayHi.apply(user);
const bound = sayHi.bind(user);
bound();
```

### 🎯 Currying

```js
function multiply(a) {
  return function (b) {
    return a * b;
  };
}
```

### 🧼 Pure Functions

```js
function add(a, b) {
  return a + b;
}
```

### ✅ Advanced Examples

```js
const counter = (() => {
  let count = 0;
  return () => ++count;
})();

function memoize(fn) {
  const cache = {};
  return function (x) {
    if (cache[x]) return cache[x];
    return (cache[x] = fn(x));
  };
}
```

### 💪 Advanced Exercises

1. Create a recursive function that calculates the nth Fibonacci number.
2. Create a function that returns a function with a private counter.
3. Write a memoized version of a slow square function.
4. Build a curried `add(a)(b)` function.

### 🧠 Advanced Solutions

```js
function fibonacci(n) {
  if (n <= 1) return n;
  return fibonacci(n - 1) + fibonacci(n - 2);
}

function privateCounter() {
  let count = 0;
  return function () {
    return ++count;
  };
}

function slowSquare(n) {
  for (let i = 0; i < 1e8; i++); // simulate delay
  return n * n;
}

function memoize(fn) {
  const cache = {};
  return function (x) {
    if (cache[x]) return cache[x];
    return (cache[x] = fn(x));
  };
}

function curriedAdd(a) {
  return function (b) {
    return a + b;
  };
}
```
---
## Real World applications of Functions
📦 1. Form Validation Function
Real-world use: Website login/registration
```js
function validateEmail(email) {
  const pattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;
  return pattern.test(email);
}

// Usage
console.log(validateEmail("user@example.com")); // true
console.log(validateEmail("userexample.com"));  // false
```
🔍 2. Search Filter Function
Real-world use: Search bar filtering on an e-commerce site
```js
function filterProducts(products, searchTerm) {
  return products.filter(product =>
    product.name.toLowerCase().includes(searchTerm.toLowerCase())
  );
}

// Usage
const items = [
  { name: "Laptop" },
  { name: "Tablet" },
  { name: "Phone" }
];

console.log(filterProducts(items, "lap")); // [{ name: "Laptop" }]
```
📅 3. Date Formatter
Real-world use: Blog post date display.
```js
function formatDate(date) {
  return new Date(date).toLocaleDateString("en-US", {
    year: "numeric",
    month: "long",
    day: "numeric"
  });
}

// Usage
console.log(formatDate("2025-06-06")); // June 6, 2025
```
📈 4. Currency Formatter
Real-world use: Displaying prices
```js
function formatCurrency(amount, currency = "USD") {
  return new Intl.NumberFormat("en-US", {
    style: "currency",
    currency
  }).format(amount);
}

// Usage
console.log(formatCurrency(2500)); // $2,500.00
console.log(formatCurrency(2500, "NGN")); // NGN 2,500.00
```
✅ 5. Todo App Toggle Function
Real-world use: Task management app
```js
function toggleTaskStatus(task) {
  return { ...task, completed: !task.completed };
}

// Usage
const task = { id: 1, text: "Learn JS", completed: false };
console.log(toggleTaskStatus(task)); // { id: 1, text: "Learn JS", completed: true }
```
📥 6. API Data Formatter
Real-world use: Displaying API responses
```js
function formatUserData(user) {
  return `${user.firstName} ${user.lastName} (${user.email})`;
}

// Usage
const apiUser = {
  firstName: "Ada",
  lastName: "Lovelace",
  email: "ada@code.com"
};

console.log(formatUserData(apiUser)); // Ada Lovelace (ada@code.com)
```
🧪 7. Utility Function — Random ID Generator
Real-world use: Create unique IDs for new items
```js
function generateId(length = 8) {
  return Math.random().toString(36).substr(2, length);
}

// Usage
console.log(generateId()); // e.g., "f9z3hdp2"

```
---

## 🏁 Final Thoughts

JavaScript functions are powerful tools — mastering them will make you a better problem solver, developer, and thinker. Practice

