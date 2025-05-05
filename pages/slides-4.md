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

# DOM

Presentation slides for developers

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

The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes) -->


---
transition: fade-out
---

# What is DOM?

<!-- Slidev is a slides maker and presenter designed for developers, consist of the following features -->

**DOM** Also known as **Document Object Model**  is a document model loaded in the browser and representing the document as a node tree or **DOM tree to (like &lt;div&gt;, &lt;p&gt;, or text)** where each node represents part of the document.
it allows JavaScript and other languages to access and manipulate the document’s content dynamically.
The DOM is one of the most-used APIs on the web because it allows code running in a browser to access and interact with every node in the document. Just like the way softwares are most used because they allow the hardware to interacts with other parts of the computer.
But in this case,Nodes can be created, moved, and changed
<br>
<br>
<!-- Read more about [Why Slidev?](https://sli.dev/guide/why) -->
The DOM can be used for different purposes which include:<br>
* MIfication<br>
* Navigation<br>
* Searching<br>

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/features/slide-scope-style
-->

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

<!--
Here is another comment.
-->

---
transition: slide-up
level: 2
---


---
layout: two-cols
layoutClass: gap-16
---

# Table of contents

<!-- You can use the `Toc` component to generate a table of contents for your slides: -->
* Modification:<br>
As said before that the Document object model interacts with the webpage UI. DOM modification
includes changing the structure, content, or style of a web page using JavaScript after the page has
loaded. This is a core part of creating interactive web pages.<br>
The set of things which we can modify:<br>


```js
//create element node
const newElem = document.createElement(&quot;span&quot;)
// Cant see it yet because we havent inserted it to the DOM
// Add content and style to the new element
newElem.innerText = "This is a Span element";
newElem.style.color = "red";
// Insert the new element to the end of body element
```

<!-- The title will be inferred from your slide content, or you can override it with `title` and `level` in your frontmatter.

::right:: -->

---
layout: image-right
layoutClass: gap-16
---

* Navigation:<br>
DOM navigation includes the process of moving through and accessing different parts of the HTML
document (like elements and nodes) using JavaScript.
Instead of the old fashion locating by query selector or by ID or Class etc.<br>
It lets you traverse the document structure, like moving from a parent to its child or from one sibling
to another.<br>
Its own way of locating is through the children nodes which is from the title downwards
Some of its capabilities include:<br>
---
layout: image-right
image: https://cover.sli.dev
---

```js {all|5|7|7-8|10|all} twoslash
// list all child nodes of the body tag
console.log(document.body.childNodes); //Note newline characters is a Text node, which is a child of the body tag

// check if the body tag has children
console.log(document.body.hasChildNodes()); // true

// loop through all children of the body tag
for (let i = 0; i < document.body.childNodes.length; i++) {
console.log(document.body.childNodes[i]);
}
```



<!-- Inline style -->
<style>
.footnotes-sep {
  @apply mt-5 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

<!--
Notes can also sync with clicks

[click] This will be highlighted after the first click

[click] Highlighted with `count = ref(0)`

[click:3] Last click (skip two clicks)
-->

---
level: 2
---

* searching: <br>
Here, finding element is done the old way, is the process of finding elements in an HTML
document using JavaScript so that you can access or modify them. This is a key part of working with
the DOM.<br>
The different ways include:<br>

````md magic-move {lines: true}
```js {*|2|*}
// Get element by ID
// const h1 = document.getElementById(&quot;h1_text&quot;)
// console.log(h1)

// // Get properties from the selected element
// console.log(h1.id) // returns "h1_text";
// console.log(h1.innerText) // returns "Hello World"
// console.log(h1.innerHTML) // returns "<h1>Hello World</h1>"
// console.log(h1.style.color) // returns "rgb(0, 0, 0)";
// console.log(h1.style.fontSize) // returns "20px"
// console.log(h1.style.backgroundColor) // returns "rgb(255, 255, 255)"
// // Get elements by class name
// const h1_class = document.getElementsByClassName("h1_class")
// console.log(h1_class)

// // Get elements by tag name
// const h1_tag = document.getElementsByTagName("h1")
// console.log(h1_tag)


```
```
````

---







# Learn More

[Documentation](https://sli.dev) · [GitHub](https://github.com/slidevjs/slidev) · [Showcases](https://sli.dev/resources/showcases)

<PoweredBySlidev mt-10 />
