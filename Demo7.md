# Demo 7: 

# Grid Boxes
```sh
* {  
box-sizing: border-box;  
}  
  
.box {  
float: left;  
width: 33.33%; /* three boxes (use 25% for four, and 50% for two, etc) */  
padding: 50px; /* if you want space between the images */  
}

<div>
  <div class="box" style="background-color:#bbb">
	  <p>Some text inside the box.</p>
  </div>
  <div class="box" style="background-color:#ccc">
	  <p>Some text inside the box.</p>
  </div>
  <div class="box" style="background-color:#ddd">
	  <p>Some text inside the box.</p>
  </div>
</div>
```
**What is box-sizing?**

You can easily create three floating boxes side by side. However, when you add something that enlarges the width of each box (e.g. **padding or borders**), the box will break. The `box-sizing` property allows us to include the padding and border in the box's total width (and height), making sure that the padding stays inside of the box and that it does not break.

# CSS Layout - display: inline-block
- `display: inline-block` allows to set a width and height on the element and the top and bottom margins/paddings are respected, but with `display: inline` they are not.
- Compared to `display: block`, the major difference is that `display: inline-block` does not add a line-break after the element, so the element can sit next to other elements.
`display: inline`, `display: inline-block` and `display: block`
```sh
display: inline; /* the default for span */
width: 100px;
height: 100px;
padding: 5px;
border: 1px solid blue;  
background-color: yellow; 
<div>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum consequat scelerisque elit sit amet consequat. Aliquam erat volutpat. <span class="a">Aliquam</span> <span class="a">venenatis</span> gravida nisl sit amet facilisis. Nullam cursus fermentum velit sed laoreet. </div>
```

## Center Align Elements
- To horizontally center a block element (like ```<div>```), use `margin: auto;`
- Setting the width of the element will prevent it from stretching out to the edges of its container.
- The element will then take up the specified width, and the remaining space will be split equally between the two margins:
```sh
margin: auto;  
width: 50%;  
border: 3px solid green;  
padding: 10px;
```

# CSS Combinators
There are four different combinators in CSS:

-   descendant selector (space)
-   child selector (>)
-   adjacent sibling selector (+)
-   general sibling selector (~)


div p --> Selects all ```<p>``` elements inside `<div>` elements
div > p --> Selects all `<p>` elements where the parent is a `<div>` element
div + p --> Selects all `<p>` elements that are placed immediately after `<div>` elements
p ~ ul -->  Selects every `<ul>` element that are preceded/after by a `<p>` element


## What are Pseudo-classes?
A pseudo-class is used to define a special state of an element.

For example, it can be used to:

-   Style an element when a user mouses over it
-   Style visited and unvisited links differently
-   Style an element when it gets focus
```a:hover``` 

    ```div:hover```
    ```p i:first-child``` Match the first `<i>` element in all `<p>` elements
## What are Pseudo-Elements?

A CSS pseudo-element is used to style specified parts of an element.

For example, it can be used to:

-   Style the first letter, or line, of an element
-   Insert content before, or after, the content of an element
```p::first-line```
```p::first-letter```
- The `::before` pseudo-element can be used to insert some content before the content of an element.
```sh
h1::before {  
content: url(smiley.gif);  
}
```
````::after````

`::selection` pseudo-element matches the portion of an element that is selected by a user.

# The `opacity` property specifies the opacity/transparency of an element.
The `opacity` property can take a value from 0.0 - 1.0. The lower value, the more transparent:

# Dropdowns
https://www.w3schools.com/css/css_dropdowns.asp

# CSS Attribute Selectors
```sh
[title~=flower] {
  border: 5px solid yellow;
}
a[target]
[attribute|="value"] [class|="top"]  select elements with the specified attribute starting with the specified value top-list
[class^="top"]  selects all elements with a class attribute value that begins with "top"
[class$="test"] selects all elements with a class attribute value that ends with "test"
[class*="te"] The `[attribute*="value"]` selector is used to select elements whose attribute value contains a specified value. selects all elements with a class attribute value that contains "te"
```
