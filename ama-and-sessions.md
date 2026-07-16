# JavaScript Interview Questions & Answers

## 1. What is the Event Loop?

The **Event Loop** is a mechanism in JavaScript that allows it to perform **non-blocking asynchronous operations** even though JavaScript is single-threaded.

### How it works:
1. JavaScript executes synchronous code from the **Call Stack**.
2. Asynchronous operations (like `setTimeout`, `fetch`, DOM events) are handled by **Browser APIs**.
3. Once completed, their callbacks are placed into the **Callback Queue** (or **Microtask Queue** for Promises).
4. The Event Loop checks if the Call Stack is empty.
5. If empty, it moves tasks from the queue to the Call Stack for execution.

> **Priority:** Microtask Queue (Promises) → Callback Queue (`setTimeout`, events)

---

## 2. Why do we use JavaScript?

JavaScript is used to make web pages **interactive and dynamic**.

### Uses:
- Handle user interactions (clicks, forms, keyboard events)
- Manipulate the DOM
- Make API requests (`fetch`, `axios`)
- Perform validations
- Build web applications
- Create backend applications using Node.js
- Develop mobile and desktop applications

---

## 3. Is JavaScript Weakly Typed or Dynamically Typed?

JavaScript is **both dynamically typed and weakly typed**.

### Dynamically Typed
The data type is determined at runtime.

```javascript
let value = 10;
value = "Hello";
value = true;
```

No type declaration is required.

### Weakly Typed
JavaScript automatically converts one data type into another when needed.

```javascript
console.log("5" + 2); // "52"
console.log("5" - 2); // 3
```

---

## 4. Describe the Flow of Promises

A Promise represents the eventual completion or failure of an asynchronous operation.

### States
- **Pending** → Initial state
- **Fulfilled** → Operation completed successfully
- **Rejected** → Operation failed

### Flow

```
Create Promise
      │
      ▼
   Pending
   /      \
Success   Failure
  │          │
then()    catch()
    \      /
     finally()
```

Example:

```javascript
fetch("https://api.example.com")
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.log(error))
  .finally(() => console.log("Completed"));
```

---

## 5. What is Variable Shadowing?

Variable shadowing happens when a variable declared inside a block or function has the **same name** as a variable in an outer scope.

The inner variable hides (shadows) the outer variable.

```javascript
let name = "John";

function test() {
    let name = "Alice";
    console.log(name); // Alice
}

test();
console.log(name); // John
```

---

## 6. When do we use the `map()` function?

`map()` is used when we want to **transform every element of an array** and return a **new array**.

Example:

```javascript
const nums = [1, 2, 3];

const doubled = nums.map(num => num * 2);

console.log(doubled);
// [2, 4, 6]
```

Use `map()` when:
- Modifying each element
- Creating a new array
- Rendering lists in React

---

## 7. Difference Between `find()` and `filter()`

| find() | filter() |
|---------|----------|
| Returns the first matching element | Returns all matching elements |
| Stops after finding one match | Checks the entire array |
| Returns an object/value or `undefined` | Returns a new array |
| Used when only one result is needed | Used when multiple results are needed |

Example:

```javascript
const numbers = [10, 20, 30, 40];

numbers.find(num => num > 20);
// 30

numbers.filter(num => num > 20);
// [30, 40]
```

---

## 8. What is a Higher-Order Function?

A **Higher-Order Function (HOF)** is a function that:
- Takes another function as an argument, or
- Returns another function.

Example:

```javascript
function greet(name) {
    return "Hello " + name;
}

function process(fn) {
    console.log(fn("John"));
}

process(greet);
```

---

## 9. Tell Some Higher-Order Functions

Common Higher-Order Functions in JavaScript:

- `map()`
- `filter()`
- `reduce()`
- `find()`
- `findIndex()`
- `some()`
- `every()`
- `sort()`
- `forEach()`
---

## 10. What is Throttling?

**Throttling** limits how many times a function can execute within a specified time interval.

It is mainly used to improve performance during frequent events.

Examples:
- Scroll event
- Resize event
- Mouse movement
- Button clicks

Example:

```javascript
window.addEventListener(
    "scroll",
    throttle(handleScroll, 300)
);
```

If throttled to **300ms**, the function runs at most once every 300 milliseconds.

---

## 11. Tell Some Browser APIs in JavaScript

Some commonly used Browser APIs are:

- DOM API
- Fetch API
- Local Storage API
- Session Storage API
- Geolocation API
- History API
- Navigator API
- Clipboard API
- Web Storage API
- Notification API
- Drag and Drop API
- WebSocket API
- Canvas API
- Audio API
- setTimeout()
- setInterval()

---

## 12. Difference Between `map()` and `forEach()`

| map() | forEach() |
|--------|-----------|
| Returns a new array | Returns `undefined` |
| Used for transforming data | Used for performing actions |
| Does not modify original array | Does not return a new array |
| Can be chained | Cannot be chained directly |
| Used when a new array is needed | Used when only iteration is needed |

Example:

### map()

```javascript
const nums = [1,2,3];

const result = nums.map(num => num * 2);

console.log(result);
// [2,4,6]
```

### forEach()

```javascript
const nums = [1,2,3];

nums.forEach(num => {
    console.log(num * 2);
});
```
