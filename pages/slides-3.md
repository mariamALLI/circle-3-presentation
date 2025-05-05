---
# You can also start simply with 'default'
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Welcome to Slidev
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

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

# Circle Three(3) member

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

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
---


# Names of circle member

**1. Mariam Alli** `contributors`

**2. Iranloye Hannah** `contributors`

**3. Omoshola Elegbede** `contributors`

**4. Adebomojo Ademola** `inactive`

**5. Idowu Olatomiwa Stephen** `contributors`

**6.Obiegbusi Emmanuel Cherechukwu**

**7.Abdulazeez Ghaniyah Omotayo** `inactive`

**8. Joanna Bassey**

**9. Chidinma Oparah** `contributors`

**10. Emmanuel Brown Okon** `inactive`


<style>
h1 {
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

# Summary About Function in programming

## Functions in JavaScript

Functions allow you to write reusable code that can be executed multiple times without duplication.

They are a core concept in JavaScript, enabling developers to encapsulate tasks such as returning values based on inputs or performing specific calculations.

Functions help organize and structure your code, making it more readable and maintainable. In JavaScript, a function is a block of code created to accomplish a specific task.

Functions play a crucial role in programming.

To define a function, use the `function` keyword.

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

## Type of Function
There are two types of functions in JavaScript:
1. **Built-in Functions**: These are functions that are already available in JavaScript and can be used.
2. **User-defined Functions**: These are functions that are created by the user to perform a specific task.


### We have function without parameters**

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

## We have function with parameters**

In JavaScript, a function with parameters is defined to accept inputs, known as parameters. When calling the function, you provide arguments that correspond to these parameters.

```javascript
Example;
function displayName(firstName, lastName) {
  alert(firstName + " " + lastName); // use + to add two values togather
}
displayName("Idowu", "Tomiwa");
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

## Function returns**

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

# callback functions

callback function are function we assigned like variables and they are function we can call insdie another function

```javascript
Example;
function displayUser(displayType, showFullName, showUserName) {
  if (displayUser == "full") {
    showFullName();
  } else {
    showUserName();
  }
}
function showFullName() {
  alert("Idowu olatomiwa");
}
function showUserName() {
  alert("idowu2345");
}
displayUser("full", showFullName, showUserName);
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


