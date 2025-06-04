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

