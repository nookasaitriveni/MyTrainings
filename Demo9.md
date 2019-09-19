
# Demo 9
# Pagination
```sh
<!DOCTYPE html>
<html>
<head>
<style>
.pagination {
  display: inline-block;
}

.pagination a {
  color: black;
  float: left;
  padding: 8px 16px;
  text-decoration: none;
}

.pagination a.active {
  background-color: #4CAF50;
  color: white;
}

.pagination a:hover:not(.active) {background-color: #ddd;}
</style>
</head>
<body>

<h2>Active and Hoverable Pagination</h2>
<p>Move the mouse over the numbers.</p>

<div class="pagination">
  <a href="#">&laquo;</a>
  <a href="#">1</a>
  <a class="active" href="#">2</a>
  <a href="#">3</a>
  <a href="#">4</a>
  <a href="#">5</a>
  <a href="#">6</a>
  <a href="#">&raquo;</a>
</div>

</body>
</html>

```
Adding borders to `.pagination a` will have more look

# Browser Specific Support
- Supported by Edge/Internet Explorer with prefix -ms-

- Supported by Firefox with prefix -moz-

- Supported by Google Chrome with prefix -webkit-

- Supported by Safari with prefix -webkit-

- Supported by Opera with prefix -webkit-
# CSS Multiple Columns

- Allows easy definition of multiple columns of **text** just like in newspapers
- The `column-count` property specifies the number of columns an element should be divided into. 
	- `column-count: 3;` This will divide the text in the element into 3 columns
- The `column-gap` property specifies the gap between the columns.
	- `column-gap: 40px;` specifies a 40 pixels gap between the columns
- The `column-rule-style` property specifies the style of the rule between columns
	- `column-rule-style: solid;` adds line between the columns
- The `column-rule-width` property specifies the width of the rule between columns
	- column-rule-width: 1px;
- The `column-rule-color` property specifies the color of the rule between columns
	- column-rule-color: lightblue;
- The `column-rule` property is a shorthand property
	- `column-rule: 1px solid lightblue;`

# CSS Custom Properties (`Variables`)
```sh
:root {
  --main-bg-color: coral;
  --main-txt-color: blue;  
  --main-padding: 15px;  
}

#div1 {
  background-color: var(--main-bg-color);
  color: var(--main-txt-color);  
  padding: var(--main-padding);
}

#div2 {
  background-color: var(--main-bg-color);
  color: var(--main-txt-color);
  padding: var(--main-padding);
}
```
# JavaScript
1. **HTML** to define the content of web pages

2. **CSS** to specify the layout of web pages

3. **JavaScript** to program the behavior of web pages

- **JavaScript** Can Change HTML Content
	- `document.getElementById("demo").innerHTML = "Hello JavaScript";`
	- *Note:-* JavaScript accepts both double and single quotes
- **JavaScript** Can Change HTML Attribute Values
	- `document.getElementById('myImage').src='pic_bulbon.gif'"`
- **JavaScript** Can Change HTML Styles (CSS)
	- `document.getElementById("demo").style.fontSize = "35px";`
- **JavaScript** Can Hide HTML Elements
	- `document.getElementById("demo").style.display = "none";`
- **JavaScript** Can Show HTML Elements
	- `document.getElementById("demo").style.display = "block";`
- It cab ve written inside Html events like onclick etc..,
- It can be written inside `<script>` tag. 
	- You can place any number of scripts in an HTML document.
	- Scripts can be placed in the `<body>`, or in the `<head>` section of an HTML page, or in both.
- Scripts can also be placed in external files (**External JavaScript**)
	- `<script src="myScript.js"></script>`
	- External scripts are practical when the same code is used in many different web pages.
	- JavaScript files have the file extension **.js**.
	- You can place an external script reference in `<head>` or `<body>` as you like.

	- The script will behave as if it was located exactly where the `<script>` tag is located.
	- *Note*: External scripts cannot contain `<script>` tags.
	- It separates HTML and code
	- It makes HTML and JavaScript easier to read and maintain
# JavaScript Output
JavaScript can "display" data in different ways:

-   Writing into an HTML element, using `innerHTML`
	- `document.getElementById("demo").innerHTML = 5 + 6;`
-   Writing into the HTML output using `document.write()`
	- `document.write(5 + 6);`
	- For testing purposes, it is convenient to use `document.write()`
	- *Note*: Using `document.write()` after an HTML document is loaded, will **delete all existing HTML**
		- `<button type="button" onclick="document.write(5 + 6)">Try it</button>`
	- The `document.write()` method should only be used for testing
-   Writing into an alert box, using `window.alert()`
	- `window.alert(5 + 6);`
	- You can use an alert box to display data 
-   Writing into the browser console, using `console.log()`
	- For debugging purposes, you can use the `console.log()` method to display data

*Note*: Semicolons(;) separate JavaScript statements.
For best readability, programmers often like to avoid code lines longer than 80 characters.

# Variable declaration
JavaScript variables are containers for storing data values.
**var** keyword is used to declare variable

    var x;
    x = 10;
    
    or
    
    var x = 10;
# Function
```sh
    function myFunction(a, b) {
        console.log('Functiona in Javascript')
        return a * b;             // Function returns the product of a and b
    }
```

