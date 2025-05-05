---
theme: seriph
title: DOM Events for Beginners
---
transition: slide-left
---

# What Are DOM Events?

DOM events are interactions or occurrences that happen within a web page, such as clicking a button, typing in a text field, or scrolling through content. These events allow your code to respond dynamically, enabling interactive and engaging user experiences.

# Common DOM Events

- `click` – when you click on something
- `mouseover` – when you hover over something
- `keydown` – when a key is pressed
- `submit` – when a form is submitted

---
transition: fade-out
---

# What Is an Event Handler?

An **event handler** is a function that is called in response to an event. 

# Ways to Attach Event Handlers

There are 3 common ways:
- HTML attribute
- DOM-property
- addEventListener method

---
transition: fade-out
--- 

# The HTML-Attribute method

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

# The drawbacks of this method is that:
- It mixes HTML and Javascript which can be quite confusing in the longrun.
- It is hard to manage when building larger scale apps.
---
transition: fade-out
---

# The DOM-Property Method

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

### Advantages:
- Keeps JavaScript separate from HTML, improving code readability.
- Easier to manage compared to inline event handlers.

### Drawbacks:
- Only one event handler can be assigned per event, as assigning a new handler overwrites the previous one.
- Less flexible compared to `addEventListener()` for handling multiple listeners.

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

### Why Use `addEventListener()`?

- **Supports multiple handlers:** You can attach multiple functions to the same event.
- **More control:** It allows you to specify options like `once`, `capture`, and `passive`.
- **Better separation of concerns:** Keeps JavaScript separate from HTML, improving maintainability.

---
transition: fade-out
---

# Understanding the Event Object

The **event object** is a special object automatically passed to your event handler when an event occurs. It provides detailed information about the event, such as the type of event, the target element, and additional data like mouse position or key pressed.

### Key Properties of the Event Object:
- **`type`**: The type of event (e.g., `click`, `keydown`).
- **`target`**: The element that triggered the event.
- **Mouse or keyboard details**: Information like mouse position or which key was pressed.

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

In this example:
- The `event.type` logs the type of event (`click`).
- The `event.target` logs the element that triggered the event (`<button>`).

By using the event object, you can make your event handlers more dynamic and responsive to user interactions.

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


