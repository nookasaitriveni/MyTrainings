# Demo10

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
# JavaScript Objects
- JavaScript objects are written with curly braces `{}`.
- Object properties are written as name:value pairs, separated by commas.
- ``` var person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}; ```
- The object (person) in the example above has 4 properties: firstName, lastName, age, and eyeColor.
- In real life, a car is an object. 
- A car has properties like weight and color
  -  ``` var car = {type:"Fiat", model:"500", color:"white"};```
  - Accessing Object Properties
    - ```objectName.propertyName``` or ``` objectName["propertyName"]```
- A car has methods like start and stop
    - Methods are actions that can be performed on objects.
    ```sh
    var person = {
      firstName: "John",
      lastName : "Doe",
      id       : 5566,
      fullName : function() {
        return this.firstName + " " + this.lastName;
      }
    };
    ```
    - ##### The ```this``` Keyword
        - In a function definition, this refers to the "owner" of the function.
        - In the example above, this is the person object that "owns" the fullName function.
        - In other words, this.firstName means the firstName property of this object.
    - ##### Accessing Object Methods
        - name = person.fullName();
        - If you access a method without the () parentheses, it will return the function definition:
- All cars have the same properties, but the property values differ from car to car.
- All cars have the same methods, but the methods are performed at different times.


Note: Any variable can be emptied, by setting the value to undefined. The type will also be undefined.
```car = undefined;    // Value is undefined, type is undefined ```

# HTML Events
An HTML event can be something the browser does, or something a user does.

Here are some examples of HTML events:
- An HTML web page has finished loading
- An HTML input field was changed
- An HTML button was clicked

Often, when events happen, you may want to do something.
JavaScript lets you execute code when events are detected.
```sh
<button onclick="document.getElementById('demo').innerHTML=Date()">The time is?</button>
<p id="demo"></p>
```
```sh
<button onclick="this.innerHTML=Date()">The time is?</button>
```
### Common HTML Events
| Event | Description |
|--|--|
|onchange |	An HTML element has been changed |
| onclick |	The user clicks an HTML element |
| onmouseover |	The user moves the mouse over an HTML element |
| onmouseout |	The user moves the mouse away from an HTML element |
| onkeydown	| The user pushes a keyboard key |
| onload |	The browser has finished loading the page |
# String Length
```sh
txt.length;
```
# Escape Character
| Code | Result |	Description |
|--|--|--|
| ```\'```|	' |	Single quote |
| ```\"``` |	"	| Double quote|
| `\\` |	`\` |	Backslash|
```
var x = "We are the so-called \"Vikings\" from the north.";
var x = "The character \\ is called backslash.";
```
*Note*:You can also break up a code line within a text string like below
```sh
document.getElementById("demo").innerHTML = "Hello " +
"Dolly!";
```
# Finding a String in a String
The indexOf() method returns the index of (the position of) the first occurrence of a specified text in a string:
*Note*: JavaScript counts positions from zero.
```sh
var str = "Please locate where 'locate' occurs!";
var pos = str.indexOf("locate");
```
The lastIndexOf() method returns the index of the last occurrence of a specified text in a string starting from begining
*Note*: Both indexOf(), and lastIndexOf() return -1 if the text is not found.
Both methods accept a second parameter as the starting position for the search:
```sh
str.indexOf("locate", 15); // this will start search for location from 15 in indexof.
in lastIndexOf this will skip last 15 letters and then it will search for the string from the beginning
```
# Slicing
There are 3 methods for extracting a part of a string:
- slice(start, end)
    - returns the extracted part in a new string
    - If a parameter is negative, the position is counted from the end of the string(-12, -6)
    - If you omit the second parameter, the method will slice out the rest of the string, this means this will start from given number till end
- substring(start, end)
    - similar to slice() main difference is that substring() cannot accept negative indexes
- substr(start, length)
    - similar to slice() main difference is that the second parameter specifies the length of the extracted part.
# Replacing String Content
```sh
str = "Please visit Microsoft!";
var n = str.replace("Microsoft", "W3Schools");
```
- The replace() method does not change the string it is called on. It returns a new string. If you want to change the existing string then assign replace to existing string variable.
- By default, the replace() method replaces only the first match
- By default, the replace() method is case sensitive. Writing MICROSOFT (with upper-case) will not work
- To replace case insensitive, use a regular expression with an /i flag (insensitive)
    - ```sh 
        str = "Please visit Microsoft!";
        var n = str.replace(/MICROSOFT/i, "W3Schools");
        ```
    - Note that regular expressions are written without quotes.
    - To replace all matches, use a regular expression with a /g flag (global match)
# Converting to Upper and Lower Case
- ``` text1.toUpperCase()```
- ```  text1.toLowerCase(); ```
# The concat() Method
- ``` concat()``` joins two or more strings
- ```sh
    var text1 = "Hello";
    var text2 = "World!";
    var text3 = text1.concat(" ",text2);
    ```
- The concat() method can be used instead of the plus operator. These two lines do the same:
    - ```sh
        var text = "Hello" + " " + "World!";
        var text = "Hello".concat(" ", "World!");
        ```
        
- All string methods return a new string. They don't modify the original string.
- Formally said: Strings are immutable: Strings cannot be changed, only replaced.
# String.trim()
- The trim() method removes whitespace from both sides of a string
- ``` var str = "       Hello World!        "; ```

# ```str.charAt(0); ``` returns character at a specified index (position) in a string
# ```str[0]``` also returns the same
    - It is read only. ```str[0] = "A"``` gives no error (but does not work!)
# If no character is found , ```[ ]``` returns undefined, while ```charAt()``` returns an empty string
