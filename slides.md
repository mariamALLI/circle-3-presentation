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

## Presentation By Circle 3

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
  background-color:#2B90B6;
  background-image:linear-gradient(45deg, #c5d44e 0%, #01b0f2 20%);;
  background-size: 100%;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5); /* X-offset, Y-offset, blur-radius, color */

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


<style>
  h1 {
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
# Table of Content (Part 2)
| **Section**                          | **Topics**                                                                 | 
|--------------------------------------|-----------------------------------------------------------------------------|
| **4. Functions**              | - Type of functions                                              |
|                                  | - Function Expression (FE)                                         |
|                                  | - Function Declaration (FD)                                        |
|                                  | - Arrow Function (AF)                                        | 


<style>
  h1 {
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
# Table of Contents (Part 3)

| **Section**                          | **Topics**                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| **5. Declaration of Array, and Object** | - Adding items into an array or object                                     |
|                                      | - Using loop to iterate over an array or object                            |
|                                      | - Types of Methods to use on an array                                      |
|                                      | - Loops                                                                    |
| **6. Making API calls**              | - Using Rest parameters and Spread syntax                                  |
|                                      | - Callback functions                                                       |
|                                      | - Promises, async and await                                                |


<style>
  h1 {
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

# Table of Content (Part 4)

| **Section**                          | **Topics**                                                                 |
|--------------------------------------|-----------------------------------------------------------------------------|
| **7. Data Structure, DOM, & Events in JavaScript** | - DOM & DOM Manipulation                                                  |
|                                      | - DOM Navigation & Searching                                               |
|                                      | - DOM Modification                                                         |
|                                      | - Browser Object Model (BOM)                                               |
|                                      | - DOM Events & Event Handlers                                              |
|                                      | - Event Listeners & Event Object                                           |

<style>
  h1 {
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

# Module in JavaScript?

Modules in JavaScript allow you to split your code into reusable pieces, making it more maintainable and easier to manage. Each module has its scope, meaning variables and functions are not shared unless explicitly exported.

```javascript
// math.js
export const add = (a, b) => a + b;
```

```javascript
// main.js
import { add } from './math.js';
console.log(add(2, 3)); // 5
```

```javascript
// multiply.js
export default function multiply(a, b) {
  return a * b;
}
```
<br>

<!--
You can have a `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

## What is Importing

Importing allows you to bring functions, variables, or classes from another module. You use the import keyword to access the exports from another JavaScript file.

```javascript
// Default import
import multiply from './math.js';
console.log(multiply(2, 5)); // 10
```
```javascript
// Importing everything
import * as math from './math.js';
console.log(math.area(5));
```
```javascript
// utils.js
export const greet = name => `Hello, ${name}!`;
// app.js
import { greet } from './utils.js';
console.log(greet("Mariam")); // Hello, Mariam!
```

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

## Dynamic Import 
Dynamic import allows you to load modules only when they are needed using the import() function. It returns a promise and is useful for performance optimization (like code splitting).

```javascript
button.addEventListener('click', async () => {
  const module = await import('./math.js');
  console.log(module.add(3, 4));
});
```
```javascript
async function loadUtil() {
  const { greet } = await import('./utils.js');
  console.log(greet('Mariam'));
}
```
```javascript
// Conditional dynamic import
if (condition) {
  import('./feature.js').then(module => {
    module.runFeature();
  });
}
```

<style>
  h2 {
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

## Form Data
The FormData object lets you easily construct a set of key/value pairs representing form fields and their values. It’s commonly used to submit forms via JavaScript, especially when working with APIs.

```javascript
const form = document.querySelector('form');
const formData = new FormData(form);
```

```javascript
formData.append('username', 'mariam');
console.log(formData.get('username')); // mariam

fetch('/submit', {
  method: 'POST',
  body: formData,
});
```

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

## The Core Method of FormData
The FormData object provides core methods such as append(), get(), set(), and entries() to manipulate and retrieve form data dynamically. These methods are especially useful for AJAX form submissions.

```javascript
const data = new FormData();
data.append('name', 'Mariam');
console.log(data.get('name')); // Mariam

data.set('name', 'Alli'); // Updates value if key exists
console.log(data.get('name')); // Alli

for (let [key, value] of data.entries()) {
  console.log(`${key}: ${value}`);
}
```

<style>
  h2 {
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

## Best Practices (FormData)
When using FormData, always validate inputs, avoid sending sensitive data in plaintext, and use appropriate HTTP headers. It’s best to let the browser set Content-Type when using FormData.

```javascript
const form = document.querySelector('#myForm');
form.addEventListener('submit', e => {
  e.preventDefault(); // Prevent default reload
  const data = new FormData(form);
});

fetch('/api', {
  method: 'POST',
  body: new FormData(document.querySelector('form')),
});
// Do NOT manually set Content-Type when using FormData
// Let the browser handle it
```

<style>
  h2 {
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

## Closure and Variable Scope
A closure is a function that retains access to its outer scope, even after the outer function has finished executing. This is closely tied to JavaScript’s function-level scope and lexical scoping.

```javascript
function outer() {
  let count = 0;
  return function inner() {
    count++;
    console.log(count);
  };
}
const counter = outer();
counter(); // 1
counter(); // 2
```

```javascript
function makeAdder(x) {
  return function(y) {
    return x + y;
  };
}
const add5 = makeAdder(5);
console.log(add5(3)); // 8
```

<style>
  h2 {
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

## Lexical Enviroment
The lexical environment is the structure that holds variable and function declarations at the time the function is defined, not executed. It forms the basis of how JavaScript scopes variables.

```javascript
function outer() {
  let name = 'Mariam';
  function inner() {
    console.log(name);
  }
  return inner;
}
const greet = outer();
greet(); // Mariam
```
```javascript
let globalVar = 'Global';
function test() {
  let localVar = 'Local';
  console.log(globalVar); // Accessible
}
test();
```

<style>
  h2 {
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

## Global Object

The global object provides built-in functions, constants, and global variables accessible from anywhere in your code. In browsers, it’s window, while in Node.js, it’s global.

```javascript
let name = 'Mariam';
console.log(window.name); // Mariam (let adds to global object)
```


## Functional Object ###
In JavaScript, functions are first-class objects. This means they can have properties and methods, be passed as arguments, returned from other functions, and stored in variables.

```javascript
function greet() {}
greet.language = 'English';
console.log(greet.language); // English
```
```javascript
const sayHi = function() {
  console.log('Hi');
};
sayHi(); // Hi
```

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

## Named Function Expression (NFE)
A Named Function Expression is when a function expression has its own name. It’s useful for recursion and debugging because the name is only available inside the function.

```javascript
const factorial = function fact(n) {
  return n <= 1 ? 1 : n * fact(n - 1);
};
console.log(factorial(5)); // 120
```

```javascript
const greet = function sayHello(name) {
  console.log(`Hello, ${name}`);
};
greet('Mariam');
```

```javascript
//with an arrow function
const greet = (name) => {
  console.log(`Hello, ${name}`);
};
greet('Mariam');
```

<style>
  h2 {
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

## The “length” Property
The length property of a function tells you how many parameters it expects. For arrays or strings, it returns the number of items or characters.

```javascript
function add(a, b) {}
console.log(add.length); // 2

const arr = [1, 2, 3];
console.log(arr.length); // 3

const greet = function(name, age, city) {};
console.log(greet.length); // 3
```

<style>
  h2 {
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


## Functions in JavaScript

Functions allow you to write reusable code that can be executed multiple times without duplication.

They are a core concept in JavaScript, enabling developers to encapsulate tasks such as returning values based on inputs or performing specific calculations.

Functions help organize and structure your code, making it more readable and maintainable. In JavaScript, a function is a block of code created to accomplish a specific task.

Functions play a crucial role in programming.

To define a function, use the `function` keyword.

## Type of Function
There are two types of functions in JavaScript:
1. **`Built-in Functions`**: These are functions that are already available in JavaScript and can be used 
2. **`User-defined Functions`**: These are functions that are created by the user to perform a specific task.

<style>
  h2 {
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
### Functions Without Parameters

In JavaScript, a function without parameters is defined and called without requiring any arguments.

```javascript
Example;
function sum() {
  let result = 20 + 30;
  console.log(`The result is ${result}`);
}
// create a function and can use / call it multiple times
sum();
```

Any variable that is declared outside the function can be accessed inside the function. The function is called a global variable.
example

```javascript
Example;
let gretting = "Hello";
function sayHi() {
  console.log(gretting); //access the global variable
}
sayHi(); //Result will be Hello
```

<style>
  h3 {
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

## Functions with Parameters

In JavaScript, a function with parameters is defined to accept inputs, known as parameters. When calling the function, you provide arguments that correspond to these parameters.

```javascript
Example;
function displayName(firstName, lastName) {
  alert(firstName + " " + lastName); // use + to add two values togather
}
displayName("Idowu", "Tomiwa");
```

<br>

## Function expression

A function expression in JavaScript is a way to define a function by assigning it to a variable.

```javascript
Example;
const justHome = function () {
  console.log("That is my House");
};
justHome(); //output That is my House
```


<style>
  h2 {
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

## Function Returns

A function with a return statement is one that provides a value or another function as its output. The `return` keyword is used within the function to specify what should be returned. Once the `return` statement is executed, the function stops running immediately. Therefore, the placement of the `return` statement within the function is crucial.

Function return example:

```javascript
Example;
function displayName(firstName, lastName) {
  const fullName = firstName + " " + lastName;
  return fullName;
}
let fullname = ("Olatomiwa", "idowu");
alert(fullname); //outcome will be Olatomiwa idowu
```

```javascript
Example;
function addTwoNumber(number1, number2) {
  const sum = number1 + number1;
  return sum;
}
const result1 = addTwoNumber(20, 30);
console.log(result1); //outcome will be 40
```

<style>
  h2 {
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

## Arrow Functions

Arrow functions in JavaScript provide a concise syntax for writing function expressions. They are widely used for their simplicity and readability.

```javascript
let sum = (a, b) => {
  a + b;
};
```

<style>
  h2 {
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



## What Are DOM Events?

DOM events are interactions or occurrences that happen within a web page, such as clicking a button, typing in a text field, or scrolling through content. These events allow your code to respond dynamically, enabling interactive and engaging user experiences.

#### Common DOM Events

- `click` – when you click on something
- `mouseover` – when you hover over something
- `keydown` – when a key is pressed
- `submit` – when a form is submitted

<style>
  h2, h4 {
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

## What Is an Event Handler?

An `event handler` is a function that is called in response to an event. 

### Ways to Attach Event Handlers

There are 3 common ways:
- HTML attribute
- DOM-property
- addEventListener method

<style>
  h2,h3 {
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

## The HTML-Attribute method

Here you assign an event to HTML elements using attributes eg assigning an onclick event to a button element.

Example :

```html
<button onclick="sayHi()">Click me</button>

<script>
  function sayHi() {
    alert('Hello!');
  }
</script>
```

### The drawbacks of this method is that:
- It mixes HTML and Javascript which can be quite confusing in the longrun.
- It is hard to manage when building larger scale apps.

<style>
  h2,h3 {
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

## The DOM-Property Method

The DOM-Property method involves assigning an event handler directly to a property of a DOM element in JavaScript. This property corresponds to the event you want to handle. When the event occurs, the browser automatically invokes the assigned function.

Example:
```html
<button id="btn">Click me</button>
<script>
  const btn = document.getElementById("btn");
  btn.onclick = function () {
    alert('Hello!');
  };
</script>
```

#### Advantages:
- Keeps JavaScript separate from HTML, improving code readability.
- Easier to manage compared to inline event handlers.

#### Drawbacks:
- Only one event handler can be assigned per event, as assigning a new handler overwrites the previous one.
- Less flexible compared to `addEventListener()` for handling multiple listeners.

<style>
  h2,h4 {
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

# Using the `addEventListener()` Method

The `addEventListener()` method is a modern and flexible way to attach event handlers to elements. It allows you to register multiple event listeners for the same event without overwriting existing ones.

### Example:

```html
<button id="btn">Click me</button>

<script>
  const btn = document.getElementById("btn");

  // First event listener
  btn.addEventListener('click', () => {
    alert('Hello!');
  });

  // Second event listener
  btn.addEventListener('click', () => {
    alert('Hello again!');
  });
</script>
```

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
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

## Why Use addEventListener() ?

- **Supports multiple handlers:** You can attach multiple functions to the same event.
- **More control:** It allows you to specify options like `once`, `capture`, and `passive`.
- **Better separation of concerns:** Keeps JavaScript separate from HTML, improving maintainability.


## Understanding the Event Object
The **event object** is a special object automatically passed to your event handler when an event occurs. It provides detailed information about the event, such as the type of event, the target element, and additional data like mouse position or key pressed.

### Key Properties of the Event Object:
- `type`: The type of event (e.g., `click`, `keydown`).
- `target`: The element that triggered the event.
- `Mouse or keyboard details`: Information like mouse position or which key was pressed.


<style>
  h2,h3 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

### Example: Logging Event Details

```html
<button id="btn">Click me</button>

<script>
  const btn = document.getElementById("btn");

  btn.addEventListener("click", function(event) {
    console.log("Event Type:", event.type);   // Logs: click
    console.log("Target Element:", event.target); // Logs: <button id="btn">Click me</button>
  });
</script>
```

#### In this example:
- The `event.type` logs the type of event (`click`).
- The `event.target` logs the element that triggered the event (`<button>`).

By using the event object, you can make your event handlers more dynamic and responsive to user interactions.

<style>
  h3,h4 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

## Event Listener vs Event Object

- *Event listener* listens for an event (eg a click)
- *Event handler* is the function that gets triggered when the event occurs—it decides what action to take in response.
- *Event object* is passed to the handler and gives details about the event, such as which element was clicked, the mouse position, or any additional details.

Analogy:
Imagine someone knocks on your door.

- The *`listener`* is you, waiting to hear the knock.
- The *`handler`* is your response—opening the door, asking who’s there, etc.
- The *`object`* is the explanation of the knock—how loud it was, how many times they knocked, etc.

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

## DOM Modification Techniques/Methods

DOM modification allows developers to dynamically interact and update the structure,style and content of a webpage,There are various methods and techniques used in manipulating a DOM.

- Text/Content Modification
- Attributes Modification
- CSS Style Modification
- Create & Replacing Elements
- Remove & RemoveChild Elements
- Insert & Append Elements

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

### Text/Content Modification

- `textContent`: This changes the text content of an element

```html
<p id="element" v-click>Old Text</p>
<script>
  document.getElementById("element").textContent = "New Text";
</script>
```

- `innerHTML`: This changes the HTML content inside an element

```html
<p id="element" v-click>Old Content</p>
<script>
  document.getElementById("element").innerHTML = "<p>New Content</p>";
</script>
```

<style>
  h3 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

## Attributes Modification

- `setAttribute`: Add or Modifies an attribute on an element

###### HTML

```html
<p id="element v-click">Old Class</p>
```

###### Css

```css
.new-class {
  color: red;
  font-size: 20px;
  text-align: center;
  text-decoration: line-through;
}
```

###### JS

```javascript
document.getElementById("element").setAttribute("class", "new-class");
```

- `removeAttribute`: Add or Modifies an attribute on an element

Example:

```javascript
     document.getElementById("element").removeAttribute("class")
```

<style>
 h2, h6 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

- `direct access to attributes`: We can also modify attributes like id,href,class,src.

~ Example:
```html
<a href="url" id="link">link text</a>

<script>
  document.getElementById("link").href = "https://www.netflix.com/ng/";
</script>
```
<br>

#### Class style Modification

- `Style property`: We can modify an element inline css  using style property

``` html 
      <p id ="element">Hello World</p>

      <script> 
          document.getElementById("element").style.color = "blue";
          document.getElementById("element").style.fontSize = "20px";
      </script>
```

- `ClassList`: Add,remove or toggle css classes dynamically

<style>
  h4,h6 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

#### Add classList:
```html
<p id ="element">Hello World</p>

 <style>
  .new-class{
            color:red;
            border:1px solid grey;
            width: 200px;
            height: 40px;
            display: flex;
            align-items: center;
            justify-content: center
        }
</style>

  <script>
      document.getElementById("element").classList.add("new-class")
  </script>
```

#### remove classList:
```js 
    document.getElementById("element").classList.remove("old-class")
```

#### Toggle classList:

```js 
    document.getElementById("element").classList.toggle("active")
```

<style>
  h4,h6 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

## Create & Replacing Elements

  - `Create() Elements`:  Creates a new HTML element dynamically.

  Example:
```js
  let newElement = document.createElement("p");
  newElement.textContent = "This is a paragraph created with createElement()";
```
<br>

- `Replacing() Elements`: Replaces an existing child element with a new one.

Example:

```html
<div id="parentElement">
    <h1 id="oldElement"> content</h1>
</div>
```
```js
let parent = document.getElementById("parentElement");
let newElem = document.createElement("p");
newElem.textContent = " new paragraph"
let oldElem = document.getElementById('oldElement');

parent.replaceChild(newElem,oldElem)
```

<style>
  h2 {
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

## Remove & RemoveChild Elements
-`RemoveChild() Elements`:  Removes a specific child element from its parent.

Example:
```html
  <div id="parentElement">
        <h1 id="childElement"> content</h1>
    </div>

    <script>
      let parent = document.getElementById('parentElement');
      let child = document.getElementById('childElement'); 
      parent.removeChild(child);
    </script>
```

-`Remove Elements()`:  Directly removes an element from the DOM.

Example:
```js
  document.getElementById('parentElement').remove()
```

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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

## Insert & Append Elements

-`insertBefore()`: Inserts a new element before a specified existing element.:
```html
  <div id="parentElement">
        <h1 id="oldElement"> content</h1>
    </div>

    <script>
      let parent = document.getElementById("parentElement");
      let newElem = document.createElement("p");
        newElem.textContent = "This paragraph is being inserted before h1";
      let existingElem = document.getElementById('oldElement');
      parent.insertBefore(newElem,existingElem);
    </script>
```

<br>

-`insertAdjacentHTML()`:  Inserts HTML content at a specified position relative to an element.

Example
```js
    document.getElementById("element").insertAdjacentHTML('beforeend',"<p>New Html content using insertAdjacentHtml </p>"
    );
```

<style>
  h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg, #c5d44e 0%, #146b8c 20%);
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


-`AppendChild() Elements`: Adds a new child element to an existing element.

```html 
     <div id="parentElement">
        <!-- The new child elements show here -->
    </div>
    <script>
         let parent = document.getElementById("parentElement");
         let childAppend = document.createElement("p");
         childAppend.textContent = "This is a new paragraph using appendChild";
         parent.appendChild(childAppend);
    </script>
```

---
transition: fade-out
---

# Browser Object Model (BOM)

The Browser Object Model (BOM) enables JavaScript to interact with the browser outside the scope of the Document Object Model (DOM). It provides objects and methods to control browser-specific features such as navigation, location, and user interaction. Key components of the BOM include:


- **Window Object**: Represents the browser window and provides methods like `alert()`, `prompt()`, and `confirm()`.
- **Navigator Object**: Provides information about the browser, such as the user agent and platform.
- **Location Object**: Allows access to and manipulation of the current URL.
- **History Object**: Enables navigation through the browser's session history.

The BOM is essential for creating dynamic and interactive web applications by leveraging browser-specific functionalities.

<style>
  h1,h2 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #146b8c 20%);
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


### Window
-`window`:understand the window object.

Example:
```html
 <p id='demo'></p>
  <!-- This shows the window's width and height -->
  <script>
        let demo = document.getElementById("demo");
        demo.innerHTML ="window width is "+ window.innerWidth +"px" + " and window Height is " + window.innerHeight +"px";
    </script>

```
<br>

### Other Window Method

-`window.open()` - open a new window

-`window.close()` - close the current window

-`window.moveTo()` - move the current window

-`window.resizeTo()` - resize the current window


<style>
  h3 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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


-`Alert`:display an alert dialog.

Example
```js
  window.alert(Message)
  alert(Message)
  // Message is a variable that contains a string that is shown to the users
```

-`Confirm`: display a modal dialog with a question and two buttons of OK and CANCEL.

Example
```js
  window.confirm("Are u sure you want to delete?");
   // It returns a boolean value OK means true CANCEL means False
```

-`Prompt`:prompt the user to input some text.

Example
```js
  let result = window.prompt(message)
  //An if statement can be used in checking the value of the message 
```


---
transition: fade-out
---


-`SetTimeOut`: set a timer and execute a callback function once the timer expires.

Example
```html
  <button onclick="timeOut()">setTimeout</button>
<script>
   function timeOut(){
        let result = alert("I love learning  a programming language");
        setTimeout(() => {
            result
        },3000)
     }
</script>
```

<br>

---
transition: fade-out
---


-`SetInterval`: execute a callback function repeatedly with a fixed delay between each call.We have clearInterval and setInterval.

Example
```html
  <p id="flashText">set interval</p>
    <button onclick="start()">start</button>
    <button onclick="stop()">stop</button>

<script>

      let intervalID;
    function toggleTextColor(){
        let e = document.getElementById('flashText');
        e.style.color = e.style.color == "red" ? "blue" : "red";
    }
    function stop(){
            clearInterval(intervalID); //Stops the toggle color
        }
        function start(){
            intervalID = setInterval(toggleTextColor,1000) 
        }

</script>
```

---
transition: fade-out
---



## Location

The `location` object provides information about the current URL of the browser and allows you to manipulate it. It is accessible via `window.location` or `document.location`, both pointing to the same object.

### Key Location Properties:

- **`href`**:  The full URL of the current page.
- **`protocol`**:  The protocol used (e.g., `http:` or `https:`).
- **`host`**: The hostname and port number of the URL.
- **`pathname`**: The path of the URL after the domain.
- **`search`**: The query string of the URL (e.g., `?id=123`).
- **`hash`**: The fragment identifier (e.g., `#section1`).

<style>
 h2, h3 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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


#### Example:

```javascript
console.log(window.location.href); // Full URL
console.log(window.location.protocol); // Protocol
console.log(window.location.host); // Hostname and port
console.log(window.location.pathname); // Path
console.log(window.location.search); // Query string
console.log(window.location.hash); // Fragment
```

<br>

#### Common Methods

- `assign(url)`: Loads a new document at the specified URL.
- `reload()`: Reloads the current page.
- `replace(url)`: Replaces the current document with a new one (does not save in history).

```js
// Navigate to a new page
window.location.assign('https://example.com');

// Reload the current page
window.location.reload();

// Replace the current page
window.location.replace('https://example.com');
```

<style>
 h4 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

# Summary of Refactoring UI Learnt So Far
1. Design individual features first before worrying about the overall layout.
 
`Example`: 
Designing the features of a flight search.
Your interface will need:
- A field for the departure city
- A field for the destination city
- A field for the departure date
- A field for the return date
- A button to perform the search

<br>

2. Detail Comes Later: Focus on functionality before adding typography, colors, and shadows. That means try working on grayscale colors to help move quickly then later you can comeback to add the necessary colors where needed. 



<style>
 h1 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

3. #### Don’t Design Too Much: 
   Avoid overdesigning every feature before development.Figuring out how every feature in a product should interact and how every edge case should look is really hard, especially in the abstract but will help move your work faster and know what is working or not during implementation.Also try build the simple design version so that implementation can be done easily. If there are extra features you want to add you can then push for it later, which means the extra feature to be added later won’t delay the simple features during deployment and implementation. 

<br>

1. #### Choose a Personality: Fonts, colors, border and language define your app’s personality.
- `FONTS`:
1. Typography plays a huge part in determining how a design feels.
2. If you want an elegant or classic look, you might want to incorporate a serif typeface font in your design. 
3. For a playful look, you could use a rounded sans serif
4. If you’re going for a plainer look, or want to rely on other elements to provide the personality, a neutral sans serif works great:


<style>
 h4 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

- `COLORS`:
You need to understand the feel of color as an individual.
1. Blue is safe and familiar — nobody ever complains about blue.
2. Gold might say “expensive” and “sophisticated”.
3. Pink is a bit more fun, and not so serious:

<br>

- `BORDER RADIUS`:
1. A small border radius is pretty neutral, and doesn’t really communicate much of a personality on its own.
2. A large border radius starts to feel more playful.
3. While no border radius at all feels a lot more serious or formal

<br>

-	`LANGUAGE`:
1. While not a visual design technique per se, the words you use in an interface have a massive influence on the overall personality.
2. Using a less personal tone might feel more official or professional.
3. While using friendlier, more casual language makes a site feel, well, friendlier:

---
transition: fade-out
---

5. #### Limit Your Choices: 
   Use a predefined set of `colors`, `fonts`, and `sizes` to make design decisions easier.
-  `Systematise Everything:`
	The more systems you have in place, the faster you’ll be able to work and the
	less you’ll second guess your own decisions. You’ll want systems for things like:
	• `Font size`
	• `Font weight`
	• `Line height`
	• `Color`
	• `Margin`
	• `Padding`
	• `Width`
	• `Height`
	• `Border radius`
	• `Border width`
	• `Opacity`

6. `Not All Elements Are Equal`:Emphasize important elements and de-emphasize secondary ones.

7. #### Size Isn’t Everything:
   Font weight and color are also useful for creating emphasis. Instead of leaving all of the heavy lifting to font size alone, try using `font weight` or `color` to do the same job.
- `Try and stick to two or three colors`:
		 A dark color for primary content (like the headline of an article)
		• A grey for secondary content (like the date an article was published)
		• A lighter grey for tertiary content (maybe the copyright notice in a
				footer) Similarly, two font weights are usually enough for UI work:
		• A normal font weight (400 or 500 depending on the font) for most text
		• A heavier font weight (600 or 700) for text you want to emphasize
 

<style>
 h4 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

8. #### Avoid Grey Text on Colored Backgrounds:
    Instead, pick a color that works well with the background. For example when you have a dark green background, the best contrast is to use a green color for the text but adjust the saturation and lightness until it looks perfect to you.

9. #### Emphasize by De-emphasizing:
     Reduce contrast or size of competing elements, so that the main element can stand out through de-emphasising other element around it.

10. #### Labels Are a Last Resort: Only use labels when necessary;
 sometimes formatting is enough to convey meaning, and the format data is written user can easily identify what is what, which gives the developer better opportunity to give respective data the emphasis when necessary. Only use labels when absolutely necessary and requied.

11. #### Separate visual hierarchy from document hierarchy:
 Usually the content in that section should be the focus, not the title. That means that a lot of the time, titles should actually be pretty small. Don’t let the element you’re using influence how you choose to style it, pick elements for semantic purposes and style them however you need to create the best visual hierarchy.


<style>
 h4 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

12. #### Balance weight and contrast: 
- `Using contrast to compensate for weight:` A simple and effective way to lower the contrast of the icon by giving it a softer color. This works anywhere you need to balance elements that have different weights. Reducing the contrast works like a counterbalance, making heavier elements feel lighter even though the weight hasn’t changed.

- `Using weight to compensate for contrast:` Just like how reducing contrast helps to 		de-emphasize heavy elements, increasing weight is a great way to add a bit of 				emphasis to low contrast elements. This is useful when things like thin 1px borders are 		too subtle using a soft color, but darkening the color makes the design feel harsh and 		noisy. Making the border a bit heavier by increasing the width helps to emphasize
		it without losing the softer look.

13. #### Semantics are secondary:
Semantics are an important part of button design, but that doesn’t mean you can forget about hierarchy.
- `Primary actions should be obvious:` Solid, high contrast background colors work great here.
- `Secondary actions should be clear but not prominent:` Outline styles or lower contrast background colors are great options.
- `Tertiary actions should be discoverable:` Styling actions like links is the best approach.

<style>
 h4 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
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

<!-- `Primary actions should be obvious:` Solid, high contrast background colors work great here.
`Secondary actions should be clear but not prominent:` Outline styles or lower contrast background colors are great options.
`Tertiary actions should be discoverable but unobtrusive:` Styling these actions like links is usually the best approach. -->