## 1. What is NPM and how it is used?
NPM (Node Package Manager) is a tool that comes with Node.js. It is used to install, update, remove and manage JavaScript libraries and dependencies in a project.

Example:
```bash
npm install express
```
## 2. Is semicolon mandatory in JS?
Semicolon is not mandatory in JavaScript because of Automatic Semicolon Insertion (ASI).
However, it is recommended to use semicolons to avoid unexpected errors.
## 3. What are different types of datatypes in JS?
**Primitive Data Types:**

- String
- Number
- Boolean
- Null
- Undefined
- BigInt
- Symbol
  
**Non-Primitive:**

- Object
- Array
- Function
## 4. What is delete command in SQL?
DELETE removes rows from a table based on a condition.

**Example:**
```
DELETE FROM users WHERE id = 5;
```
## 5. JS is a single threaded language then how it performs asynchronous operations?
JavaScript runs in a single thread, but asynchronous tasks are handled using:
- Event Loop
- Callback Queue
- Web APIs
- Promises and async/await
These allow JS to perform tasks like API calls and timers without blocking the main thread.

## 6. What is the use of meta tag?
Meta tags provide information about the webpage to browsers and search engines.

**Example:**
```html
<meta name="description" content="My website">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
## 7. Difference between pass by value and pass by reference?
**Pass by Value**

A copy of the value is passed. Changing inside function does not affect original.

**Pass by Reference**

Reference (memory address) is passed. Changing inside function affects original data.

## 8. What is module in JS?
A module is a reusable piece of code that can be imported and exported between files.

**Example:**
```js
export function add() {}
import { add } from './math.js'
```
## 9. What is LIMIT in SQL?
LIMIT is used to restrict the number of rows returned in a query.

**Example:**
```sql
SELECT * FROM users LIMIT 5;
```
## 10. How many selectors are there in CSS?
Common selectors:
- Element selector
- Class selector
- ID selector
- Attribute selector
- Pseudo-class selector
- Pseudo-element selector
- Universal selector
## 11. What is the difference between slice and splice?
**slice()**

Does not modify original array. Returns a new array.
```js
arr.slice(1,3)
```
**splice()**

Modifies original array. Can add/remove elements.
```js
arr.splice(1,2)
```
## 12. What is object in JS?
An object is a collection of key-value pairs used to store structured data.

**Example:**
```js
const user = {
  name: "Hima",
  age: 21
}
```
