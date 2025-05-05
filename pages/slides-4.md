---
theme: seriph
class: text-white
background: https://raw.githubusercontent.com/mdn/content/main/files/en-us/web/api/document_object_model/dom_tree.png
layout: cover
transition: slide-up
---


# Understanding the DOM and BOM

A developer's guide to the Document Object Model and browser object model 
Presented with 💙 using Slidev

---

# What is the DOM?

**DOM = Document Object Model**

- Structured representation of HTML
- Browser parses HTML into a **tree**
- Nodes = elements like `<div>`, `<p>`
- JavaScript can manipulate it dynamically

```html
<body>
  <h1>Hello</h1>
  <p>Welcome</p>
</body>
```

Becomes this DOM tree structure:

- <code>document</code>
  - <code>html</code>
    - <code>head</code>
    - <code>body</code>
      - <code>h1('Hello')</code>
      - <code>p('Welcome to my page')</code>

---
transition:fade-out
---

## Why the DOM is Important

- Enables JavaScript to interact with the page by reading, modifying, adding, or removing content.

- Brings dynamism and interactivity to your website.

- Browsers provide access to the DOM through the `document` object, for example:
  <br>
  <code>document.querySelector("p").textContent = "Updated!";</code>


## Navigating the DOM

DOM navigation allows you to traverse the tree structure:

🔹 Parent, Child, and Sibling Nodes

- <code>parentNode</code>: Access the immediate parent node.

- <code>childNodes</code>: Retrieve all child nodes, including text, comment, and element nodes.

- <code>children</code>: Get only the child element nodes.

- <code>firstChild</code> / <code>lastChild</code>: Access the first or last child node (includes text nodes).

- <code>firstElementChild</code> / <code>lastElementChild</code>: Access the first or last child element node.

- <code>nextSibling</code> / <code>previousSibling</code>: Navigate to the next or previous sibling node (includes text nodes).

- <code>nextElementSibling</code> / <code>previousElementSibling</code>: Navigate to the next or previous sibling element node.

---
transition: fade-out
---


# Searching the DOM (Selectors)

| Method                          | Purpose                              |
| ------------------------------- | ------------------------------------ |
| `getElementById(id)`            | Quickly retrieves **a single element** by its ID. |
| `getElementsByClassName(class)` | Returns an **HTMLCollection** of elements with the specified class. |
| `getElementsByTagName(tag)`     | Retrieves all elements with the given tag name. |
| `querySelector(selector)`       | Returns the **first element** that matches the CSS selector. |
| `querySelectorAll(selector)`    | Returns a **NodeList** of all elements matching the CSS selector. |


# Examples

```js
const app = document.getElementById("app");
const messages = document.getElementsByClassName("message");
const paragraphs = document.getElementsByTagName("p");
const firstMsg = document.querySelector(".message");
const allMsgs = document.querySelectorAll(".message");
```

---
transition: fade-out
---


# DOM Modification

Once you find elements, you can **change** them or add new stuff.

## Examples

🔹 Changing content:

```js
para.textContent = "Updated Text"; // just the text
```

🔹 Changing attributes:

```js
const link = document.querySelector("a");

link.href = "https://example.com";
link.setAttribute("target", "_blank");
link.getAttribute("href"); // get current href
link.removeAttribute("target");
``` 
---

🔹 Creating / Inserting Elements:

```js
const newDiv = document.createElement("div");
newDiv.textContent = "I'm new!";
document.body.appendChild(newDiv); // adds to end of body

const container = document.querySelector("#app");
container.insertBefore(newDiv, container.firstElementChild); // insert at top
```
---
transition: fade-out
---


You can also use:

```js 
element.append()     // accepts Node or text
element.prepend()
element.before()
element.after()
element.replaceWith()
```
🔹 Removing Elements:
```js
const unwanted = document.querySelector(".remove-me");
unwanted.remove();
```

---

🔹  Modify All Paragraphs:
```js
document.querySelectorAll("p").forEach((p) => {
  p.style.color = "red";
  p.textContent += " [Updated]";
});

```

 🔹 Cloning an element:
 ```js
const elemToClone = document.querySelector("h1")
const clonedElem = elemToClone.cloneNode(true)
document.body.append(clonedElem)
```

---
transition: fade-out
---


### Why DOM APIs Are Essential (Searching, Modification, and Navigation)

These methods empower you to:

* Enhance interactivity (e.g., toggle menus, switch themes)

* React to user events (e.g., clicks, hovers, form submissions)

* Dynamically create and update content (e.g., to-do lists, cards, modals)


---
transition: fade-out
---

# 🌐 What is the BOM?
 The **Browser Object Model (BOM)** is a set of **objects provided by the browser** that lets JavaScript **interact with the browser itself**, not just the web page (like the DOM).

While the **DOM** deals with the content (HTML/XML), the **BOM** deals with the **browser window and environment**.

# Key BOM Objects & What They Do:

🪟<code>window</code>

* The **global object** in a browser.

* Everything (DOM, timers, alerts, location, etc.) hangs off <code>window</code>.

🌍<code>navigator</code>

*  Gives information about the browser.

---

---


<!-- # Learn More

<!-- [Documentation](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/resources/showcases) -->

<!-- <PoweredBySlidev mt-10 /> -->
