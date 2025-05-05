---
theme: seriph
title: DOM Modification ,BOM (Browser Object Model)
transition: slide-left
---

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

# DOM Modification Techniques/Methods

DOM modification allows developers to dynamically interact and update the structure,style and content of a webpage,There are various methods and techniques used in manipulating a DOM.

- Text/Content Modification
- Attributes Modification
- CSS Style Modification
- Create & Replacing Elements
- Remove & RemoveChild Elements
- Insert & Append Elements

## Text/Content Modification

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

---
transition: fade-out
---


## Attributes Modification

- `setAttribute`: Add or Modifies an attribute on an element

### HTML

```html
<p id="element v-click">Old Class</p>
```

### Css

```css
.new-class {
  color: red;
  font-size: 20px;
  text-align: center;
  text-decoration: line-through;
}
```

### JS

```js
document.getElementById("element").setAttribute("class", "new-class");
```

---
transition: fade-out
---

- `removeAttribute`: Add or Modifies an attribute on an element

Example:

```JS
     document.getElementById("element").removeAttribute("class")
```

- `direct access to attributes`: We can also modify attributes like id,href,class,src.

Example:

```html
<a href="url" id="link">link text</a>

<script>
  document.getElementById("link").href = "https://www.netflix.com/ng/";
</script>
```

---
transition: fade-out
---

## Class style Modification
- `Style property`: We can modify an element inline css  using style property
``` html 
      <p id ="element">Hello World</p>

      <script> 
          document.getElementById("element").style.color = "blue";
          document.getElementById("element").style.fontSize = "20px";
      </script>
```

- `ClassList`: Add,remove or toggle Css classes dynamically

### Add classList:
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
### remove classList:
```js 
    document.getElementById("element").classList.remove("old-class")
```
### Toggle classList:
```js 
    document.getElementById("element").classList.toggle("active")
```

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
-`insertAdjacentHTML()`:  Inserts HTML content at a specified position relative to an element.

Example
```js
    document.getElementById("element").insertAdjacentHTML('beforeend',"<p>New Html content using insertAdjacentHtml </p>"
    );
```

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
Browser Object Model (BOM) allows javascript interact with the browser,  BOM provides objects that expose the web browser’s functionality.

## Window
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

---
transition: fade-out
---


## Other Window Method

-`window.open()` - open a new window

-`window.close()` - close the current window

-`window.moveTo()` - move the current window

-`window.resizeTo()` - resize the current window

---
-`Alert`:display an alert dialog.

Example
```js
  window.alert(Message)
  alert(Message)
  // Message is a variable that contains a string that is shown to the users
```
---

transition: fade-out
---

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


-`SetTimeOut`:set a timer and execute a callback function once the timer expires.

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
We can access location by referencing the location properties of the window and document object, window.location and document.location leads to the same location properties.
#### Location Properties

-`Location.href` 

-`Location.protocol`

-`Location.host` 

-`Location.port` 

-`Location.pathname` 

-`Location.search` 

-`Location.hash` 

-`Location.origin` 

-`Location.username` 

-`Location.password` 

-`replace()` 

-`reload() `

---
transition: fade-out
---


## Screen
The Screen object provides the attributes of the screen on which the current window is being rendered.

```js
window.screen
```
### Screen properties
-`Height`: Represents the pixel height of the screen.

-`width`:	Represents the pixel width of the screen.

-`Top`: Represents the pixel distance of the current screen’s top.

-`pixelDepth`: A read-only that returns the bit depth of the screen.

-`colorDepth`: A read-only property that returns the number of bits used to represent colors.

-`availWidth`: A read-only property that returns the pixel width of the screen minus system elements.

---
transition: fade-out


## History
When a web browser is launched and a new webpage is opened a new web history is created,The history stack stores the current page and previous pages that you visited.


```js
window.history
```

### Methods of Navigation
-`Back()`: It works like when you click the Back button.
```js
  window.history.back()

  history.back()
```

-`Forward()`: It works like when you click the Forward button.
```js
  window.history.forward()

  history.forward()
```

---
transition: fade-out
---


-`Go()`: This allows the browser move to a specific URL in the history.
```js
    // To move Forward,works same as forward()
  window.history.go(1)

    // To move Backward,works same as Backward()
  window.history.go(-1)

  // To move to current page
  window.history.go(0)
  window.history.go()
  // To determine the number of URL in an history stack
  history.length
```

---
transition: fade-out
---



## Navigator

The `navigator` object provides information about the browser and the device running the script. It is part of the Browser Object Model (BOM) and contains properties and methods that allow you to interact with the browser environment.

### Key Navigator Properties:
- **`userAgent`**: Returns a string containing information about the browser, version, and operating system.
- **`platform`**: Provides the platform on which the browser is running (e.g., "MacIntel", "Win32").
- **`language`**: Indicates the language of the browser (e.g., "en-US").
- **`online`**: Returns a boolean indicating whether the browser is online.
- **`geolocation`**: Provides access to the device's geographical location.

### Example:
```javascript
console.log(navigator.userAgent); // Browser and OS details
console.log(navigator.platform); // Platform details
console.log(navigator.language); // Browser language
console.log(navigator.online); // Online status
```
---
transition: fade-out
---


```js
//Detecting Browser Details:
if (navigator.userAgent.includes("Chrome")) {
    console.log("You are using Chrome!");
}

//Checking Online Status:
if (navigator.online) {
    console.log("You are online!");
} else {
    console.log("You are offline!");
}

//Accessing Geolocation:
navigator.geolocation.getCurrentPosition(
    position => {
        console.log(`Latitude: ${position.coords.latitude}`);
        console.log(`Longitude: ${position.coords.longitude}`);
    },
    error => {
        console.error("Error getting location:", error);
    }
);
```