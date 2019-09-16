
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
# Local Variables
```sh
// code here can NOT use carName

function myFunction() {
  var carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName 
```

Variables declared within a JavaScript function, become LOCAL to the function.

Local variables can only be accessed from within the function.
 # How to declare variables
    var x, y, z; // "declaring" variables.
- After the declaration, the variable has no value (technically it has the value of `undefined`).
- In computer programs, variables are often declared without a value. The value can be something that has to be calculated, or something that will be provided later, like user input.

**Rules**:
- JavaScript does not interpret **VAR** or **Var** as the keyword **var**.
-   Names can contain letters, digits, underscores, and dollar signs.
-   Names must begin with a letter
-   Names can also begin with $ and _
-   Names are case sensitive (y and Y are different variables)
-   Reserved words (like JavaScript keywords) cannot be used as names
- Hyphens are not allowed in JavaScript. They are reserved for subtractions.(first-name)
Use **Underscore**(first_name), **Upper Camel Case**(FirstName) and **Lower Camel Case**(firstName) *recommended
- Strings are written inside double or single quotes. Numbers are written without quotes.
- If you put a number in quotes, it will be treated as a text string.
- Also we can use a variable to replace text in a element
- `var person = "John Doe", carName = "Volvo", price = 200;` One Statement, Many Variables
# How to assign values

    x = 5; y = 6;

# How to compute values

    z = x + y;


# Comments
Code after double slashes `//` or between `/*` and `*/` is treated as a **comment**.

# case sensitive
The variables `lastName` and `lastname`, are two different variables

# Operators
| Operator | Description |
|--|--|
| + | Addition |
| - | Subtraction |
| * | Multiplication |
|** | Exponentiation(Power) |
|/|Division|
| % |Modulus (Division Remainder)|
|++|Increment|
| - -| Decrement |

# JavaScript Comparison Operators
| Operator | Description |
|--|--|
| == | equal to |
|===|equal value and equal type |
| != | not equal |
| !== |not equal value or not equal type|
| > | greater than |
| < | less than |
| >= | greater than or equal to |
| <= | less than or equal to |
| ? | ternary operator |

# JavaScript Logical Operators
| Operator | Description |
|--|--|
| && | logical and |
| `||` | logical or |
| ! |logical not |

# JavaScript Type Operators
| Operator |Description|
|--|--|
|typeof|Returns the type of a variable (`typeof "John"` // Returns "string"  `typeof 3.14` // Returns "number")|
|instanceof|Returns true if an object is an instance of an object type|

# Data types

    var length = 16; // Number  
    var lastName = "Johnson"; // String  
    var x = {firstName:"John", lastName:"Doe"}; // Object

- When adding a number and a string, JavaScript will treat the number as a string.
	- JavaScript will treat `var x = 16 + "Volvo";` as `var x =  "16" + "Volvo";`
# JavaScript Arrays
- `var cars = ["Saab", "Volvo", "BMW"];`
- Array indexes are zero-based, which means the first item is [0], second is [1], and so on.
- Changing an Array Element ```cars[0] = "Opel";```
- cars.length;
- Accessing the Last Array Element ```cars[cars.length - 1];```
# Looping Array Elements
```sh
for (i = 0; i < fruits.length; i++) {
  console.log(fruits[i]);
}
            (OR)
fruits.forEach(myFunction);
function myFunction(value) {
  console.log(value);
}           
```
- Adding Array Elements ```fruits.push("Lemon");```
- The Difference Between Arrays and Objects
    - In JavaScript, arrays use numbered indexes.  
    - In JavaScript, objects use named indexes.
    - Arrays are a special kind of objects, with numbered indexes.
- To check if a variable is array or not (```Array.isArray(fruits); ```)
- Converting Arrays to Strings ```fruits.toString()``` output would be ```Banana,Orange,Apple,Mango```
- The join() method also joins all array elements into a string, but it can add symbols
    - ```fruits.join(" * ")``` output would be ``` Banana * Orange * Apple * Mango ```
- #### Popping and Pushing in Arrays
    - When you work with arrays, it is easy to remove elements and add new elements.
    - This is what popping and pushing is
    - Popping items out of an array, or pushing items into an array.
    - ##### Popping
        - The ```pop()``` method removes the last element from an array
        - ```fruits.pop();```
        - we can also assign this to a variable, where it will stroes the removed last element from an array
    - ##### Pushing
        - The ```push()``` method adds a new element to an array (at the end)
        - fruits.push("Kiwi"); 
        - we can also assign this to a variable, where it will stores the length of the new array
- #### Shifting Elements
    - Shifting is equivalent to popping, working on the first element instead of the last.
    - The shift() method removes the first array element and "shifts" all other elements to a lower index.
    - ```fruits.shift();```
    - we can also assign this to a variable, where it will stroes the removed first element from an array
- #### UnShifting
- The unshift() method adds a new element to an array (at the beginning)
- ```fruits.unshift("Lemon");``` // Adds a new element "Lemon" to fruits as a first element
- we can also assign this to a variable, where it will stores the length of the new array
- #### Deleting Elements
    - ```delete fruits[0];      ```     // Changes the first element in fruits to undefined
    - Using delete may leave undefined holes in the array. Use pop() or shift() instead.
- #### Merging (Concatenating) Arrays
    - ```A.concat(B)``` or multiple --> ```arr1.concat(arr2, arr3);``` or custom --> ```arr1.concat(["Emil", "Tobias", "Linus"])```
    - The concat() method does not change the existing arrays. It always returns a new array.
- #### Slicing
    - ```fruits.slice(3)``` //this will remove the first 3 elements
    - The slice() method creates a new array. It does not remove any elements from the source array
