


# CSS Intro (Cascading Style Sheets)
- CSS describes how HTML elements are to be displayed on screen, paper, or in other media.
- How to add css to a HTML element
  - Inline
    - Example: ``` <h1 style='color:red;'> Hello World! </h1> ```
  - Internal: using ```<style>``` tag inside ```<head>```
  - External - by using an external CSS file
    - ``` <link rel="stylesheet" href="styles.css"> ```
# Commonly used ``` CSS ``` (Cascading Style Sheets) Stylings    
```sh
background-color:powderblue;
color:blue;
font-family:verdana;
font-size:300%;
text-align:center;
border:2px solid Tomato;
float:left; //for images
background-image:url('clouds.jpg');
```

# Padding
  - space between the text and the border
  
# Margin
  - space outside the border
  
# Id Attribute
- To define a specific style for one special element
- Note this should be ```Unique```
- Example: ``` id="myId" ```
 
 # Class Attribute
 - To define style for group of elements
 - Example: ``` class="myClass" ```
 - 
# Colors
- color names(Tomato, Orange  )
- RGB(red green blue)(range--> 0, 255)(Decimal Values)
  - Example (255, 0, 0)--> this will generate a red color as it got red max value and green, blue as 0
- RGBA (255, 0, 0, 0.5) this will add 50% transparent 
- HEX - Hexa Decimal Value (#rrggbb) (range 00, ff)
- HSL (hue, saturation, lightness)
  - Hue is a degree on the color wheel from 0 to 360. 0 is red, 120 is green, and 240 is blue.

  - Saturation is a percentage value, 0% means a shade of gray, and 100% is the full color.

  - Lightness is also a percentage, 0% is black, 50% is neither light or dark, 100% is white
- HSLA(hsla(9, 100%, 64%, 0.2) --> 0.2 transparance)

- The alpha parameter is a number between 0.0 (fully transparent) and 1.0 (not transparent at all)

# Disabled keyword

# Text Formatting Elements
```sh
<b> - Bold text
<strong> - Important text
<i> - Italic text
<em> - Emphasized text
<mark> - Marked text <-- this is link yellow highter
<small> - Small text
<del> - Deleted text <-- stiked
<ins> - Inserted text <-- underline
<sub> - Subscript text
<sup> - Superscript text
```

# Bi-Directional text
- this will help in reversing a given text
```sh
Hello World
```
- this will be displayed as
```sh
dlroW olleH
```

# Links
-   An unvisited link is underlined and blue
-   A visited link is underlined and purple(a:visited)
-   An active link is underlined and red(a:active)
- a:hover
# Attaching Image to link
```sh
 <a href="google.com">
  <img src="image.png" alt="my image">
</a> 
```
# adding title to link using title attribute
 ```sh
 <a href="google.com" title="Gooogle here">Visit our HTML Tutorial</a> 
 ```

# Creating a bookmark or jumping to an Element
```sh
<h1 id="MyId">Hello World</h1>
<a href="MyId">Jump to Hello World</a>
```

# Paths
* reading images from a path
* redirecting urls to same path

# Tables(``` table, tr--> tableRow , th --> tableHeader, td --> tableData ```)
```sh
<table style="width:100%">  
	<tr>  
		<th>Employee</th>   
		<th>Age</th>  
	</tr>  
	<tr>  
		<td>Test</td>  
		<td>30</td>  
	</tr>  
	<tr>  
		<td>asesa</td>  
		<td>20</td>  
	</tr>  
</table>
<!-- border: 3px solid black;
border-collapse: collapse;
padding: 15px;
text-align: left;
 -->
```
- to merge columns use ``` colspan``` and for rows ``` rowspan```
- caption tag is used to add caption to a table
	- Example: `<caption>Heading</caption>` this should be inside table tag
# ```<ul>``` list-style-type styles
- disc
- circle
- square
- none (Nothing displayed)

# ```<ol>``` type styles
- 1 (1,2,3)
- A (A,B,C)
- a (a,b,c)
- I (I, II, III)
- i (i,ii,iii)
# Start for ```<ol>```
- start="10" --> this is used to start the list from 10 instead of 0

# Nested list
```sh
<ul>  
	<li>Coffee</li>  
	<li>Tea  
	<ul>  
		<li>Black tea</li>  
		<li>Green tea</li>  
	</ul>  
	</li>  
	<li>Milk</li>  
</ul>
```

# To display list horizontally
- `float:left` or `display:inline`

# display:block; --> Block Elements
- Always starts on a new line and takes up the full width available (stretches out to the left and right as far as it can).
- ``` <div> </div> ```
- Div element is often used for container for other elements

# display:inline; --> Inline Elements
- An inline element does not start on a new line and only takes up as much width as necessary.
- ```<h1> Hello all this is <span style='color:red;'>Hello World</span></h1>```
- The `<span>` element is often used as a container for some text.

