# Demo 6
```
display:none vs visibility:hidden
width vs max-width(will handle small screen)
div.ex1 {  
width:  500px;  
margin:  auto;  
border:  3px solid #73AD21;  
}  
  
div.ex2 {  
max-width:  500px;  
margin:  auto;  
border:  3px solid #73AD21;  
}
```


# The `position` property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky)

# Static
- Static positioned elements are not affected by the top, bottom, left, and right properties.
- An element with `position: static;` is not positioned in any special way; it is always positioned according to the normal flow of the page:
# Relative
- An element with `position: relative;` is positioned relative to its normal position.
- Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. **Other content will not be adjusted to fit into any gap left by the element**.
	```sh
	position:  relative;  
	left:  30px;  
	border:  3px solid #73AD21;
	```
# Fixed
- An element with `position: fixed;` is positioned relative to the viewport, which means it **always stays in the same place even if the page is scrolled**. The top, right, bottom, and left properties are used to position the element.
- **A fixed element does not leave a gap in the page where it would normally have been located.**
```sh
position:  fixed;  
bottom:  0;  
right:  0;  
width:  300px;  
border:  3px solid #73AD21;
```
# Absolute
- An element with `position: absolute;` is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).
```sh
div.relative {  
position:  relative;  
width:  400px;  
height:  200px;  
border:  3px solid #73AD21;  
}  
  
div.absolute {  
position:  absolute;  
top:  80px;  
right:  0;  
width:  200px;  
height:  100px;  
border:  3px solid #73AD21;  
}
<div class="relative">This div element has position: relative;
  <div class="absolute">This div element has position: absolute;</div>
</div>
```
# Sticky
- An element with `position: sticky;` is positioned based on the user's scroll position.
```sh
position: sticky;
top: 0px;
padding: 5px;
background-color: #cae8ca;
border: 2px solid #4CAF50;
```

# z-index
- When elements are positioned, they can overlap other elements.

The  `z-index`  property specifies the stack order of an element (which element should be placed in front of, or behind, the others).
```sh
img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
}
<h1>This is a heading</h1>
<img src="w3css.gif" width="100" height="140">
<p>Because the image has a z-index of -1, it will be placed behind the text.</p>
```
# Overflow
The `overflow` property specifies whether to clip the content or to add scrollbars when the content of an element is too big to fit in the specified area.
-   `visible`  - Default. The overflow is not clipped. The content renders outside the element's box if it is more
-   `hidden`  - The overflow is clipped, and the rest of the content will be invisible
-   `scroll`  - The overflow is clipped, and a scrollbar is added to see the rest of the content
-   `auto`  - Similar to  `scroll`, but it adds scrollbars only when necessary
```sh
  background: #4CAF50;
  color: white;
  padding: 15px;
  width: 50%;
  height: 100px;
  overflow: scroll;
  border: 1px solid #ccc;
```
- The `overflow-x` and `overflow-y` properties specifies whether to change the overflow of content just horizontally or vertically (or both)

# inherit
- this will inherit the styling from the parent
# Float

 - The CSS `float` property specifies how an element should float.
	 ```sh
	 <p>
	 <img src="pineapple.jpg" alt="Pineapple" style="float: right;width:170px;height:170px;margin-left:15px;">
	Some text
	</p>
	 ```
