---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: JavaScript Knowledge Summary.
info: |
  ## Slidev Starter Template
  Circle 3 Presentation.

  Learn more at [Sli.dev](https://sli.dev)
# apply unocss classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true

# open graph
# seoMeta:
#  ogImage: https://cover.sli.dev
---

# JavaScript Summary Presentation

Presentation By Circle 3

<div @click="$slidev.nav.next" class="mt-12 py-1" hover:bg="white op-10">
  Press Space for next page <carbon:arrow-right />
</div>

<div class="abs-br m-6 text-xl">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="slidev-icon-btn">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<style>
h1 {
  background-color:rgb(57, 206, 171);
  background-image: linear-gradient(45deg,rgb(78, 212, 127) 10%,rgba(106, 140, 20, 0.79) 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
---
transition: fade-out
---

# Table of Content (Part 1)

| **Section**                          | **Topics**                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| **1. Module in JavaScript**          | - What are modules?                                                        |
|                                      | - What is Importing                                                        |
|                                      | - Dynamic Import                                                           |
| **2. Form Data**                     | - The Core Method of Form Data                                             |
|                                      | - Best Practices                                                           |
| **3. Closure and Variable Scope**    | - Lexical Environment                                                      |
|                                      | - Global Object                                                            |
|                                      | - Function Object                                                          |
|                                      | - Named Function Expression (NFE)                                          |
|                                      | - The “length” property                                                    |

---
transition: fade-out
---

# Table of Content (Part 2)

| **Section**                          | **Topics**                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| **4. Declaration of Array, and Object** | - Adding items into an array or object                                     |
|                                      | - Using loop to iterate over an array or object                            |
|                                      | - Types of Methods to use on an array                                      |
|                                      | - Loops                                                                    |
| **5. Making API calls**              | - Using Rest parameters and Spread syntax                                  |
|                                      | - Callback functions                                                       |
|                                      | - Promises, async and await                                                |
---
transition: fade-out
---

# Table of Content (Part 3)

| **Section**                          | **Topics**                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| **6. Data Structure, DOM, & Events in JavaScript** | - DOM & DOM Manipulation                                                  |
|                                      | - DOM Navigation & Searching                                               |
|                                      | - DOM Modification                                                         |
|                                      | - Browser Object Model (BOM)                                               |
|                                      | - DOM Events & Event Handlers                                              |
|                                      | - Event Listeners & Event Object                                           |
---
transition: fade-out
---

<v-clicks animate=''>

# Arrays        

An Array in Javascript is a data structure used to store multiple values in a single variable. These values can be of any types: numbers, strings, objects, or even other arrays. Arrays in Javascript are 0-based indexed. This means the first element is at index 0, the second at index 1 and so on. 

```javascript
// Empty Array Declaration
// Declaration with square bracket
const emptyArray = [];
// Declaration using Array Constructor
const anotherEmptyArray = new Array();
```

```javascript
// Array declaration using array literal (recommended)
const fruits = ['apple', 'banana', 'orange'];
console.log(fruits[0]); // Output: 'apple'
```

```javascript
// Array declaration using Array constructor
const numbers = new Array(1, 2, 3, 4, 5);
console.log(numbers.length); // Output: 5
```

```javascript
// Array with mixed data types
const mixedArray = ['text', 42, true, {name: 'John'}, [1, 2, 3]];
```
</v-clicks>
---
transition: fade-out
---

<v-clicks animate=''>

# Array Methods       

### push( ) - Add to end of an Array
Adds one or more elements to the end of an array and returns the new length.

```javascript
const fruits = ['apple', 'banana'];
fruits.push('orange'); 

// ['apple', 'banana', 'orange']
```

### pop() - Remove from end of an Array
Removes the last element from an array and returns that element.

```javascript
const fruits = ['apple', 'banana', 'orange'];
const last = fruits.pop(); 

// last = 'orange', fruits = ['apple', 'banana']
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### shift() - Remove from start of an Array
Removes the first element from an array and returns that element.

```javascript
const fruits = ['apple', 'banana', 'orange'];
const first = fruits.shift(); 
// first = 'apple', fruits = ['banana', 'orange']
```

### unshift() - Add to start of an Array
Adds one or more elements to the beginning of an array and returns the new length.

```javascript
const fruits = ['banana', 'orange'];
fruits.unshiftt('apple')
// fruits = 'apple', 'banana', 'orange'
```

### concat() – Merge Arrays
Combines two or more arrays and returns a new array (does not modify originals).

```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
const merged = arr1.concat(arr2); // [1, 2, 3, 4]
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### slice() – Extract a portion of an Array
Returns a shallow copy of a portion of an array (start to end, end not included).

```javascript
const numbers = [1, 2, 3, 4, 5];
const subArray = numbers.slice(1, 4); // [2, 3, 4]
```

### splice() – Add/Remove elements at any position
Modifies an array by adding, removing, or replacing elements.

```javascript
const numbers = [1, 2, 3, 4, 5];
numbers.splice(2, 1, 'a', 'b'); // Removes 1 element at index 2, adds 'a' and 'b'
// Result: [1, 2, 'a', 'b', 4, 5]
```

### map() – Transform each element on an Array
Creates a new array by applying a function to each element.

```javascript
const numbers = [1, 2, 3];
const doubled = numbers.map(num => num * 2); // [2, 4, 6]
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### sort() – Order Elements
Sorts elements in place (default: lexicographical order).

```javascript
const fruits = ['banana', 'apple', 'orange'];
fruits.sort(); // ['apple', 'banana', 'orange']
```

### reverse() – Flip the Array order
Reverses the order of elements in place.

```javascript
const numbers = [1, 2, 3];
numbers.reverse(); // [3, 2, 1]
```

### reduce() – Compute a single value from Array
Reduces an array to a single value using an accumulator.

```javascript
const numbers = [1, 2, 3, 4];
const sum = numbers.reduce((acc, curr) => acc + curr, 0); // 10
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### includes() 
Checks if an element exists (returns true/false).

```javascript
const fruits = ['🍎', '🍌', '🍊'];
console.log(fruits.includes('🍊')); // true
```

### filter()
Returns all elements matching a condition.

```javascript
const numbers = [5, 12, 8, 130, 44];
const allBigNums = numbers.filter(num => num > 10); // [12, 130, 44]
```

### forEach() – Loop Through Elements
Executes a function for each array element (no return value).

```javascript
const fruits = ['🍎', '🍌', '🍊'];
fruits.forEach(fruit => console.log(fruit)); // Logs each fruit
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

# Objects

In Javascript, an object is a collection of key-value pairs, where keys (also called properties) are strings and values can be any data type, including other objects or functions.

## Creating an Object

```javascript
    // Declaration with square curly bracket or braces
    const emptyObject = {};
    // Declaration using Array Constructor
    const anotherEmptyObject = new Object();
```

```javascript
// Object declaration using object literal (recommended)
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
    isStudent: false,
};
```

```javascript
// Object declaration using Object constructor
    const car = new Object();
    car.make = 'Toyota';
    car.model = 'Camry';
    car.year = 2020;

```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## Accessing Properties of an Object

In Javascript, you can access the properties of an Object using dot (.) notation or square [] bracket notation

### Dot Notation
Use when the property name is valid identifier

```javascript
// Object declaration using object literal (recommended)
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
    isStudent: false,
};

console.log(person.firstName)
console.log(person.lastName)
console.log(person.age)
console.log(person.isStudent)
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### Square Bracket Notation

Use when the property name is dynamic, contains spaces or starts with a number and can also be used to access properties with valid identifier

```javascript
// Object declaration using object literal (recommended)
const person = {
    firstName: 'John',
    "car model": "Camry"
};

console.log(person[firstName])
console.log(person["car model"])
```

Both notations are commonly used, depending on the situation.

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## Object with nested Object

An Object can also contain other objects 

```javascript
const car = {
    brand: 'Toyota',
    specification: {
        horsepower: 300,
        fuelType: 'Gasoline'
    }
}
```

## Object with Method

Objects can obtain both properties and methods. A method is a function defined as a property of an object, Methods can perform actions using the object's data, often accessed with the {this} keyword. 

```javascript
// Object declaration using object literal (recommended)
const user = {
    name: 'Alice',
    great: function () {
        console.log(`Hello, I'm ${this.name}`);
    }
};
user.great();
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

# Loops

Loops allow you to execute a block of code repeatedly. JavaScript provides several types of loops for different use cases. Below's a breakdown of each with examples

## 1. for Loop
Best for when you know how many times you want to loop.

```javascript
for (initialization; condition; increment) {
  // code to run
}

for (let i = 0; i < 5; i++) {
  console.log(i); // 0, 1, 2, 3, 4
}
```

## 2. while Loop

Runs while a condition is true. Best when the number of iterations is unknown.

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

```javascript
while (condition) {
  // code to run
}

let i = 0;
while (i < 5) {
  console.log(i); // 0, 1, 2, 3, 4
  i++;
}
```

## 3. do...while Loop
Similar to while, but runs at least once before checking the condition.

```javascript
do {
  // code to run
} while (condition);

let i = 0;
do {
  console.log(i); // 0 (even if condition is false)
  i++;
} while (i < 0);
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## 4. for...of Loop
Iterates over iterable array
```javascript
for (const element of iterable) {
  // code to run
}

const fruits = ['🍎', '🍌', '🍊'];
for (const fruit of fruits) {
  console.log(fruit); // '🍎', '🍌', '🍊'
}
```

## 5. for...in Loop
Iterates over enumerable properties of an object (keys).

```javascript
for (const key in object) {
  // code to run
}

const person = { name: 'John', age: 30 };
for (const key in person) {
  console.log(key, person[key]); 
  // "name John", "age 30"
}
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

# Rest and Spread Operators in JavaScript

JavaScript provides two powerful operators that use the same syntax (...) but serve different purposes:

1. Spread Operator (...): Expands an iterable (array, string, object) into individual elements.

2. Rest Operator (...): Collects multiple elements into a single variable (mostly used in functions)


#  Spread Operator (...)
Used to expand elements from an iterable (arrays, objects, strings).

## Use Cases:
### A. Copying & Merging Arrays

```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

// Copy an array
const copy = [...arr1]; // [1, 2, 3]
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

```javascript
// Merge arrays
const merged = [...arr1, ...arr2]; // [1, 2, 3, 4, 5, 6]

// Insert elements
const newArr = [0, ...arr1, 4]; // [0, 1, 2, 3, 4]
```

### B. Copying & Merging Objects

```javascript
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };

// Copy an object
const copy = { ...obj1 }; // { a: 1, b: 2 }

// Merge objects (later properties overwrite earlier ones)
const merged = { ...obj1, ...obj2 }; // { a: 1, b: 2, c: 3, d: 4 }

// Add new properties
const updated = { ...obj1, e: 5 }; // { a: 1, b: 2, e: 5 }
```

### C. Converting Strings to Arrays

```javascript
const str = "hello";
const chars = [...str]; // ['h', 'e', 'l', 'l', 'o']
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

#   Rest Operator (...) 
Used to collect remaining elements into a single variable (mostly in function parameters).

## Use Cases:
### A. Function Parameters

```javascript
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}

sum(1, 2, 3); // 6
sum(5, 10, 15, 20); // 50
```

### B. Destructuring Arrays

```javascript
const nums = [1, 2, 3, 4, 5];

const [first, second, ...rest] = nums;
console.log(first); // 1
console.log(second); // 2
console.log(rest); // [3, 4, 5]
```

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### C. Destructuring Objects

```javascript
const user = { name: "John", age: 30, city: "NY" };

const { name, ...rest } = user;
console.log(name); // "John"
console.log(rest); // { age: 30, city: "NY" }
```


### Combining Both

```javascript
function logNames(first, ...others) {
  console.log(first); // "Alice"
  console.log(others); // ["Bob", "Charlie"]
}

const names = ["Alice", "Bob", "Charlie"];
logNames(...names); // Spread in call, rest in function
```

</v-clicks>

---
transition: fade-out
---

# Differences between Spread and Rest Operators

| **Operator**                          | **Differences**                                                            |
|--------------------------------------|-----------------------------------------------------------------------------|
| **Spread Operator (...)**            | - Expands Elements                                                          |
|                                      | - Objects, Arrays and Function Calls                                        |
|                                      | - Example: ({...obj}  [...arr] )                                            |
| **Rest Operator (...)**              | - Collects elements                                                         |
|                                      | - Function parameters, destructuring                                        |
|                                      | - Example: function(...args)                                                |


---
transition: fade-out
---

<v-clicks animate=''>

# Callback Functions in Javascript 

A callback function is a function passed into another function as an argument and executed later some operation completes. Callbacks are essential for:

- Asynchronous operations (e.g. setTimeout, fetch)

- Event handling (e.g. addEventListener)

- Higher-order functions (e.g. map, filter, forEach)

## Example: Simple Callback

```javascript
function greet(name, callback) {
  console.log(`Hello, ${name}!`);
  callback(); // Execute the callback
}

function sayGoodbye() {
  console.log("Goodbye!");
}

greet("Alice", sayGoodbye);
// Output: "Hello, Alice!" "Goodbye!"
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

# Why use Callbacks?

## A. Handling Asynchronous Operation

JavaScript is single-threaded (only execute one piece of code at a time), so callbacks help manage async tasks like:

- Timers (setTimeout, setInterval)

- API calls (fetch, XMLHTTPRequest)

```javascript
//Example
setTimeout(() => {
  console.log("This runs after 2 seconds"); //Callback, Execute after 2 seconds
}, 2000);
```

## B. Event Listeners
Callbacks respond to user interactions (clicks, keypresses, etc.).

```javascript
button.addEventListener("click", () => {
  console.log("Button clicked!");
});
```
</v-clicks>

---
transition: fade-out
---
<v-clicks animate=''>

## C. Array Methods

Many array methods accept callbacks:

```javascript
//Example
const numbers = [1, 2, 3];
numbers.forEach(num => console.log(num * 2)); // 2, 4, 6
```

# Types of Callbacks
### A. Synchronous Callbacks
They are callbacks that are executed immediately (e.g., Array.map, Array.filter).

```javascript
const doubled = [1, 2, 3].map(num => num * 2); // [2, 4, 6]
```

### B. Asynchronous Callbacks
Executed after an async operation (e.g., setTimeout, fetch).

```javascript
fetch("https://api.example.com/data")
  .then(response => response.json()) // Callback
  .then(data => console.log(data)); // Another callback
```


<style>
h1, h2, h3 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
</v-clicks>

---
transition: fade-out
---
<v-clicks animate=''>

# Making API Calls in JavaScript: Promises, async/await, and Error Handling
API calls are how you fetch or send data to servers. In JavaScript, this is commonly done using fetch() or libraries like Axios. Calls can be GET, POST, PUT, or DELETE based on the operation.

Modern JavaScript offers multiple methods for managing API calls effectively. Below is a detailed overview of the key approaches:

## Making API Calls with XMLHttpRequest (XHR)
XMLHttpRequest (XHR) is a legacy method for making HTTP requests in JavaScript, widely used before the introduction of `fetch` and `libraries like axios`. While modern applications favor fetch or axios for their simplicity and features, understanding XHR remains valuable for working with older codebases.

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## 1. Basic GET Request with XHR

```javascript
const xhr = new XMLHttpRequest();
xhr.open('GET', 'https://api.example.com/data', true); // Async=true

xhr.onload = function() {
  if (xhr.status >= 200 && xhr.status < 300) {
    const data = JSON.parse(xhr.responseText);
    console.log(data);
  } else {
    console.error('Request failed:', xhr.statusText);
  }
};

xhr.onerror = function() {
  console.error('Network error');
};

xhr.send();
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## 2. POST Request with XHR

```javascript
const xhr = new XMLHttpRequest();
xhr.open('POST', 'https://api.example.com/data', true);
xhr.setRequestHeader('Content-Type', 'application/json');

xhr.onload = function() {
  if (xhr.status >= 200 && xhr.status < 300) {
    console.log(JSON.parse(xhr.responseText));
  } else {
    console.error('Error:', xhr.statusText);
  }
};

xhr.onerror = function() {
  console.error('Request failed');
};

const postData = JSON.stringify({ username: 'john', age: 30 });
xhr.send(postData);
```
</v-clicks>

---
transition: fade-out
---
<v-clicks animate=''>

# The Fetch API 

The Fetch API provides a modern and promise-based approach for making network requests in JavaScript, such as retrieving resources from a server. It serves as a more streamlined and powerful alternative to the older XMLHttpRequest (XHR) method, offering improved readability and ease of use.

## Basic Syntax
```javascript
fetch(url, options)
  .then(response => {
    // handle the response
  })
  .catch(error => {
    // handle errors
  });
```

## Key Features

- Promise-based: Returns a Promise that resolves to the Response object

- Simpler syntax: Cleaner and more intuitive than XHR

- Modern features: Supports streaming, request/response objects, and more

</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## 1. Making a GET Request Fetch API


```javascript
fetch('https://api.example.com/data')
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    return response.json(); // parses JSON response
  })
  .then(data => {
    console.log(data); // handle the data
  })
  .catch(error => {
    console.error('There was a problem:', error);
  });
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## 1. Making a POST Request with Fetch API


```javascript
fetch('https://api.example.com/data', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({key: 'value'}), // data to send
})
.then(response => response.json())
.then(data => console.log(data))
.catch(error => console.error('Error:', error));
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## Error Handling

The Fetch API does not reject the promise for HTTP error statuses (such as 404 or 500); it only rejects on network failures. To handle HTTP errors, you need to check the `response.ok` property or the `response.status` code.


```javascript
fetch(url)
  .then(response => {
    if (!response.ok) {
      throw new Error(`HTTP error! status: ${response.status}`);
    }
    return response.json();
  })
  // ...
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

## Async and Await with try...catch

The `async/await` syntax provides a modern and cleaner approach to managing asynchronous operations in JavaScript. It simplifies code readability compared to traditional callbacks or chaining Promises with .then(). Using `try...catch `alongside `async/await` ensures robust error handling.

### Basic Syntax
An async function always returns a Promise, and await pauses execution until the Promise resolves.

```javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Error:', error);
  }
}

fetchData();
```
</v-clicks>

<style>
 h1, h2,h3, h4 {
     background-color: #2B90B6;
  background-image: linear-gradient(45deg, #c5d44e 0%, #8c1488f7 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
  }
  </style>


---
transition: fade-out
---

<v-clicks animate=''>

### Handling Different HTTP Errors
Not all failed HTTP requests throw an error automatically (e.g., 404 or 500). You should check response.ok or response.status.

```javascript
async function getUser(userId) {
  try {
    const response = await fetch(`https://api.example.com/users/${userId}`);
    
    if (!response.ok) { // Checks for 4xx/5xx errors
      throw new Error(`HTTP error! Status: ${response.status}`);
    }
    
    const user = await response.json();
    console.log(user);
  } catch (error) {
    console.error('Failed to fetch user:', error);
  }
}

getUser(123);
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### POST Request with async/await

```javascript
async function createUser(userData) {
  try {
    const response = await fetch('https://api.example.com/users', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify(userData),
    });

    if (!response.ok) {
      throw new Error(`HTTP error! Status: ${response.status}`);
    }

    const newUser = await response.json();
    console.log('User created:', newUser);
  } catch (error) {
    console.error('Failed to create user:', error);
  }
}

createUser({ name: 'John', age: 30 });
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

### Multiple API Calls in Parallel (Promise.all)
If you need to fetch multiple endpoints at once, use Promise.all

```javascript
async function fetchMultipleData() {
  try {
    const [usersResponse, postsResponse] = await Promise.all([
      fetch('https://api.example.com/users'),
      fetch('https://api.example.com/posts'),
    ]);

    if (!usersResponse.ok || !postsResponse.ok) {
      throw new Error('One or more requests failed');
    }

    const users = await usersResponse.json();
    const posts = await postsResponse.json();

    console.log('Users:', users);
    console.log('Posts:', posts);
  } catch (error) {
    console.error('Failed to fetch data:', error);
  }
}

fetchMultipleData();
```
</v-clicks>

---
transition: fade-out
---

<v-clicks animate=''>

# Best Practices

### Always Use try/catch
- Ensures errors are caught and handled gracefully.
- Prevents unhandled Promise rejections.

### Check response.ok in fetch
- fetch only rejects on network failures, not HTTP errors (404, 500).
- Manually check response.ok or response.status.


### Use async/await with Promise.all for Parallel Requests
- Improves performance by running multiple requests simultaneously.

# Summary
- async/await + try/catch → Best for clean, readable async code.

- Always check response.ok in fetch → HTTP errors don’t auto-reject.

- Use Promise.all for parallel requests → Faster than sequential calls.
</v-clicks>


---
transition: fade-out
---