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
|                                      | - What is Importing & Exporting                                                      |
|                                      | - Dynamic Import                                                           |
| **2. Form Data**                     | - The Core Method of Form Data                                             |
|                                      | - Best Practices                                                           |
| **3. Closure and Variable Scope**                                                   | - Global Object                                                            |
|                                      | - Function Object                                                                                                                                                    |


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

Modules in JavaScript enable code to be divided into reusable and maintainable pieces. Each module has its own scope, ensuring variables and functions remain private unless explicitly exported.
<br>

## What is Importing & Exporting
Importing and exporting in JavaScript allow you to share and reuse code across different files, making your code modular and maintainable.

#### Examples of export

```js
// utils.js
// Named export
export const greet = name => `Hello, ${name}!`;

// Default export
export default function multiply(a, b) {
  return a * b;
}
```

<style>
h1, h2,h3,h4 {
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
#### Examples of Import

`Default Import`
Used to import the default export from a file.

```js
// app.js
import multiply from './utils.js';
console.log(multiply(2, 5)); // 10
```

`Named Import`
Used to import specific named exports.

```js
// app.js
import { greet } from './utils.js';
console.log(greet("Mariam")); // Hello, Mariam!
```

`Import Everything`
Used to import all exports from a file as a single object.

```js
// app.js
import * as utils from './utils.js';
console.log(utils.greet("Mariam")); // Hello, Mariam!
console.log(utils.default(3, 4)); // 12
```

This modular approach helps organize your code and makes it easier to maintain and test.



<style>
  h2,h3, h4 {
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
Dynamic import enables loading modules on demand using the `import()` function. It returns a promise, making it ideal for performance optimization, such as code splitting.

```javascript
button.addEventListener('click', async () => {
  const module = await import('./math.js');
  console.log(module.add(3, 4));
});
```

<br>

## Form Data
The FormData object simplifies the creation of key/value pairs representing form fields and their values. It is particularly useful for submitting forms programmatically via JavaScript, especially when interacting with APIs.

```javascript
const form = document.querySelector('form');
const formData = new FormData(form);
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

#### Example using append() & get() method

```javascript
formData.append('username', 'mariam');
console.log(formData.get('username')); // mariam

fetch('/submit', {
  method: 'POST',
  body: formData,
});
```

### Core Methods of FormData
The FormData object provides methods such as `append()`, `get()`, `set()`, and `entries()` to efficiently handle and retrieve form data, making it suitable for dynamic form submissions and AJAX requests.

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
  h4,h3 {
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

## Best Practices (FormData)
Validate inputs, avoid sending sensitive data in plaintext, and let the browser handle Content-Type headers.

```javascript
const form = document.querySelector('#myForm');
form.addEventListener('submit', e => {
  e.preventDefault(); // Prevent default reload
  const data = new FormData(form);
});

fetch('/api', {
  method: 'POST',
  body: new FormData(form)
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

## Global Object

The global object serves as a container for built-in functions, constants, and global variables accessible throughout your code. In browsers, this object is `window`, while in Node.js, it is `global`.

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

## Functions in JavaScript
Functions are reusable blocks of code designed to perform specific tasks. They help organize, structure, and maintain code by encapsulating logic that can be executed multiple times. Defined using the `function` keyword, functions are essential for creating modular and readable programs in JavaScript.

There are two types of functions in JavaScript:
1. **`Built-in Functions`**: These are functions that are already available in JavaScript and can be used 
2. **`User-defined Functions`**: These are functions that are created by the user to perform a specific task.
   
<br>

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

## Functions with Parameters

Functions in JavaScript can accept inputs called parameters. These parameters allow you to pass data into the function when calling it, enabling dynamic behavior based on the provided arguments.

### Example:

```javascript
Example;
function displayName(firstName, lastName) {
  alert(`${firstName} ${lastName}`)
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

Functions with a `return` statement output a value or another function. The `return` keyword halts execution immediately, making its placement critical.

#### Example:

```javascript
Example;
function displayName(firstName, lastName) {
  const fullName = firstName + " " + lastName;
  return fullName;
}
let fullname = ("Olatomiwa", "idowu");
alert(fullname); //outcome will be Olatomiwa idowu
```

## Arrow Functions

Arrow functions in JavaScript provide a concise syntax for writing function expressions. They are widely used for their simplicity and readability.

```javascript
let sum = (a, b) => {
 return a + b;
};
sum(3, 5) // 8
```

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


<v-clicks animate=''>

# Arrays        

An array in JavaScript is a data structure that stores multiple values in a single variable. These values can be of any type, such as numbers, strings, objects, or even other arrays. Arrays are zero-indexed, meaning the first element is at index 0, the second at index 1, and so on.

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

<v-clicks animate=''>

### Array Methods 
Arrays in JavaScript have several methods that can be used to manipulate and access their elements.

#### push( ) & pop()
The push() methos adds an elements to the end of an array and returns the new length.
The pop() method removes the last element from an array and returns the removed element.

```javascript
const fruits = ['apple', 'banana'];
fruits.push('orange'); 
// ['apple', 'banana', 'orange']
```

```javascript
const fruits = ['apple', 'banana', 'orange'];
const last = fruits.pop(); 
// last = 'orange', fruits = ['apple', 'banana']
```

### shift()
Removes the first element from an array and returns that element.

```javascript
const fruits = ['apple', 'banana', 'orange'];
const first = fruits.shift(); 
// first = 'apple', fruits = ['banana', 'orange']
```

</v-clicks>

<style>
  h2,h3,h4 {
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

### slice() – Extract a portion of an Array
Returns a shallow copy of a portion of an array (start to end, end not included).

```javascript
const numbers = [1, 2, 3, 4, 5];
const subArray = numbers.slice(1, 4); // [2, 3, 4]
```

</v-clicks>

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


<v-clicks animate=''>

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

### sort() – Order Elements
Sorts elements in place (default: lexicographical order).

```javascript
const fruits = ['banana', 'apple', 'orange'];
fruits.sort(); // ['apple', 'banana', 'orange']
```

</v-clicks>

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

<v-clicks animate=''>

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

### includes() 
Checks if an element exists (returns true/false).

```javascript
const fruits = ['🍎', '🍌', '🍊'];
console.log(fruits.includes('🍊')); // true
```

</v-clicks>

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


<v-clicks animate=''>

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


<v-clicks animate=''>

## Objects

In JavaScript, an object is a collection of key-value pairs where keys (properties) are strings, and values can be any data type, including other objects or functions. Objects are used to store and organize data, making it easy to access and manipulate.

### Creating an Object
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

<style>
  h1,h2,h3 {
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

## Accessing Properties of an Object

In Javascript, you can access the properties of an Object using dot (.) notation or square [] bracket notation
### Dot Notation
Use dot notation when the property name is a valid JavaScript identifier.

```javascript
// Object declaration using object literal (recommended)
const person = {
    firstName: 'John',
    lastName: 'Doe',
    age: 30,
};

console.log(person.firstName)
console.log(person.lastName)
console.log(person.age)
```

</v-clicks>

<style>
  h3,h2 {
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

### Square Bracket Notation

Square bracket notation is useful when the property name is dynamic, includes spaces, starts with a number, or when accessing properties with valid identifiers.

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



<v-clicks animate=''>

### Object with nested Object

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

### Object with Method

Objects can have both properties and methods. A method is a function defined as a property of an object. Methods can perform actions using the object's data, often accessed with the `this` keyword.

```javascript
const user = {
  name: 'Alice',
  greet: function () {
    console.log(`Hello, I'm ${this.name}`);
  }
};

user.greet(); // Output: Hello, I'm Alice
```

</v-clicks>

<style>
  h3,h4 {
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

# Loops

Loops enable the repeated execution of a block of code. JavaScript offers various types of loops tailored for specific scenarios:

1. **for Loop**: Ideal when the number of iterations is known.
  ```javascript
  for (let i = 0; i < 5; i++) {
    console.log(i); // 0, 1, 2, 3, 4
  }
  ```

2. **while Loop**: Executes as long as a condition is true, suitable for unknown iteration counts.
  ```javascript
  let i = 0;
  while (i < 5) {
    console.log(i); // 0, 1, 2, 3, 4
    i++;
  }
  ```

3. **do...while Loop**: Runs at least once before checking the condition.
  ```javascript
  let i = 0;
  do {
    console.log(i); // 0
    i++;
  } while (i < 0);
  ```

</v-clicks>

<style>
  h2,h1 {
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

4. **for...of Loop**: Iterates over iterable objects like arrays.
  ```javascript
  const fruits = ['🍎', '🍌', '🍊'];
  for (const fruit of fruits) {
    console.log(fruit); // '🍎', '🍌', '🍊'
  }
  ```

5. **for...in Loop**: Iterates over the enumerable properties of an object.
  ```javascript
  const person = { name: 'John', age: 30 };
  for (const key in person) {
    console.log(key, person[key]); // "name John", "age 30"
  }
  ```


</v-clicks>

<style>
  h2,h1 {
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

## Rest and Spread Operators in JavaScript

JavaScript provides two versatile operators, both using the `...` syntax but serving distinct purposes:

1. **`Spread Operator (...):`** Expands elements from an iterable (e.g., arrays, objects, strings) into individual elements.
2. **`Rest Operator (...):`** Collects multiple elements into a single variable, often used in function parameters.

#### Spread Operator Use Cases:
```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];

// Copy an array
const copy = [...arr1]; // [1, 2, 3]
```
```javascript
// Merge arrays
const merged = [...arr1, ...arr2]; // [1, 2, 3, 4, 5, 6]

// Insert elements
const newArr = [0, ...arr1, 4]; // [0, 1, 2, 3, 4]
```


</v-clicks>

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

<v-clicks animate=''>


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

<v-clicks animate=''>

## Rest Operator (...)
The rest operator is used to gather the remaining elements into a single variable, often utilized in function parameters.


### Use Cases:
#### A. Function Parameters

```javascript
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}

sum(1, 2, 3); // 6
sum(5, 10, 15, 20); // 50
```

#### B. Destructuring Arrays

```javascript
const nums = [1, 2, 3, 4, 5];

const [first, second, ...rest] = nums;
console.log(first); // 1
console.log(second); // 2
console.log(rest); // [3, 4, 5]
```

</v-clicks>

<style>
  h2,h3,h4 {
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

# Differences between Spread and Rest Operators

| **Operator**           | **Description**                                                                 |
|------------------------|---------------------------------------------------------------------------------|
| **Spread Operator**    | - Expands elements from arrays, objects, or function calls.                     |
|                        | - Example: `{...obj}`, `[...arr]`.                                              |
| **Rest Operator**      | - Collects multiple elements into a single variable (e.g., function parameters).|
|                        | - Example: `function(...args)`.                                                |

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

<v-clicks animate=''>

## Callback Functions in JavaScript

A callback function is a function passed as an argument to another function and executed after a specific operation completes. They are crucial for:

- **Asynchronous operations**: Examples include `setTimeout` and `fetch`.
- **Event handling**: Used in methods like `addEventListener`.
- **Higher-order functions**: Utilized in array methods like `map`, `filter`, and `forEach`.

### Example: Simple Callback

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

<v-clicks animate=''>

## Why Use Callbacks?

### Managing Asynchronous Operations
JavaScript is single-threaded, so callbacks handle async tasks like:
- **Timers**: `setTimeout`, `setInterval`
- **API Calls**: `fetch`, `XMLHTTPRequest`

```javascript
setTimeout(() => {
  console.log("This runs after 2 seconds");
}, 2000);
```

### Event Listeners
Callbacks respond to user interactions such as clicks or keypresses.

```javascript
button.addEventListener("click", () => {
  console.log("Button clicked!");
});
```

</v-clicks>

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

<v-clicks animate=''>

## Making API Calls in JavaScript: Promises, async/await, and Error Handling

API calls enable communication with servers to fetch or send data. JavaScript provides tools like `fetch()` and libraries such as Axios to handle these operations, including GET, POST, PUT, and DELETE requests.

### Key Approaches:

1. **Promises**: Use `.then()` and `.catch()` to handle asynchronous operations.
2. **async/await**: Simplifies asynchronous code, making it more readable and easier to manage.
3. **Error Handling**:
  - Use `try...catch` with `async/await` for robust error management.
  - Check `response.ok` or `response.status` in `fetch()` to handle HTTP errors.
4. **Parallel Requests**: Use `Promise.all` for simultaneous API calls to improve performance.

These methods ensure efficient and maintainable API interactions in modern JavaScript applications.
</v-clicks>

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


<v-clicks animate=''>

## The Fetch API 

The Fetch API is a modern, promise-based method for making network requests in JavaScript. It simplifies retrieving resources from a server and offers a cleaner, more readable alternative to the older XMLHttpRequest (XHR) approach.

#### Basic Syntax
```javascript
fetch(url, options)
  .then(response => {
    // handle the response
  })
  .catch(error => {
    // handle errors
  });
```

#### Key Features

- Promise-based: Returns a Promise that resolves to the Response object

- Simpler syntax: Cleaner and more intuitive than XHR

- Modern features: Supports streaming, request/response objects, and more

</v-clicks>

<style>
  h2,h3,h4 {
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

### Making a GET Request Fetch API

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

### Making a POST Request with Fetch API

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
  h2,h3, h4 {
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

<style>
  h2,h3, h4 {
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

<style>
  h2,h3, h4 {
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



## Best Practices for Making API Calls
- async/await + try/catch → Best for clean, readable async code, Prevents unhandled Promise rejections.

- Always check response.ok in fetch → HTTP errors don’t auto-reject.

- Use Promise.all for parallel requests → Faster than sequential calls.

## What is the DOM?

The DOM (Document Object Model) is a programming interface for HTML and XML documents. It represents the structure of a web page as a tree of nodes, where each HTML element is a node. This allows programs to dynamically modify the page's structure, style, and content.


```html
<body>
  <h1>Hello</h1>
  <p>Welcome</p>
</body>
```

<style>
 h2, h3, h4 {
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



Becomes this DOM tree structure:

- <code>document</code>
  - <code>html</code>
    - <code>head</code>
    - <code>body</code>
      - <code>h1('Hello')</code>
      - <code>p('Welcome to my page')</code>

<br>

### Why the DOM is Important

- Enables JavaScript to interact with the page by reading, modifying, adding, or removing content.

- Brings dynamism and interactivity to your website.

- Browsers provide access to the DOM through the `document` object, for example:
  <code>document.querySelector("p").textContent = "Updated!";</code>


<style>
 h2, h3, h4 {
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


### Navigating the DOM

DOM navigation allows you to traverse the tree structure:

🔹 Parent, Child, and Sibling Nodes

- <code>parentNode</code>: Access the immediate parent node.

- <code>childNodes</code>: Retrieve all child nodes, including text, comment, and element nodes.

- <code>children</code>: Get only the child element nodes.

- <code>firstChild</code> / <code>lastChild</code>: Access the first or last child node (includes text nodes).

- <code>firstElementChild</code> / <code>lastElementChild</code>: Access the first or last child element node.

- <code>nextSibling</code> / <code>previousSibling</code>: Navigate to the next or previous sibling node (includes text nodes).

- <code>nextElementSibling</code> / <code>previousElementSibling</code>: Navigate to the next or previous sibling element node.



<style>
 h2, h3, h4 {
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


### Searching the DOM (Selectors)

| Method                          | Purpose                              |
| ------------------------------- | ------------------------------------ |
| `getElementById(id)`            | Quickly retrieves **a single element** by its ID. |
| `getElementsByClassName(class)` | Returns an **HTMLCollection** of elements with the specified class. |
| `getElementsByTagName(tag)`     | Retrieves all elements with the given tag name. |
| `querySelector(selector)`       | Returns the **first element** that matches the CSS selector. |
| `querySelectorAll(selector)`    | Returns a **NodeList** of all elements matching the CSS selector. |


### Why DOM APIs Are Essential (Searching, Modification, and Navigation)

* Enhance interactivity (e.g., toggle menus, switch themes)

* React to user events (e.g., clicks, hovers, form submissions)

* Dynamically create and update content (e.g., to-do lists, cards, modals)


<style>
 h2, h3, h4 {
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
Common DOM Events are:

- `click` – when you click on something
- `mouseover` – when you hover over something
- `keydown` – when a key is pressed
- `submit` – when a form is submitted

## What Is an Event Handler?

An `event handler` is a function that is called in response to an event. There are 3 common ways:
- HTML attribute
- DOM-property
- addEventListener method

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

# Using the addEventListener() Method

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

## DOM Modification Techniques/Methods

DOM modification allows developers to dynamically interact and update the structure,style and content of a webpage,There are various methods and techniques used in manipulating a DOM.

- Text/Content Modification & Attributes Modification
- CSS Style Modification & Create & Replacing Elements
- Remove & RemoveChild Elements & Insert & Append Elements

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
  h2,h3,h4 {
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

4. #### Choose a Personality: Fonts, colors, border and language define your app’s personality.

5. #### Systematise Everything:
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

6. #### Avoid Grey Text on Colored Backgrounds:
    Instead, pick a color that works well with the background. For example when you have a dark green background, the best contrast is to use a green color for the text but adjust the saturation and lightness until it looks perfect to you.

7.  #### Semantics are secondary:
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

### Names of circle member

**1. Mariam Alli** `contributors`

**2. Iranloye Hannah** `contributors`

**3. Omoshola Elegbede** `contributors`

**4. Adebomojo Ademola** `contributors`

**5. Idowu Olatomiwa Stephen** `contributors`

**6. Joanna Bassey** `contributor`

**7. Chidinma Oparah** `contributors`

**8. Emmanuel Brown Okon** `inactive`

**9.Obiegbusi Emmanuel Cherechukwu** `inactive`

**10.Abdulazeez Ghaniyah Omotayo** `inactive`

<style>
 h2,h3 {
      background-color: #2B90B6;
      background-image: linear-gradient(45deg,#c5d44e 0%, #8c1488f7 25%);
      background-size: 100%;
      -webkit-background-clip: text;
      -moz-background-clip: text;
      -webkit-text-fill-color: transparent;
      -moz-text-fill-color: transparent;
  }
</style>
