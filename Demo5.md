# Demo 5
```sh
body {
  background-image: url("img_tree.png");
  background-repeat: no-repeat;
  background-position: right top;
  margin-right: 200px;
  background-attachment: fixed or scroll;
}

background-repeat:  repeat-x or repeat-yor no-repeat;

// seperate side borders
border-top-style: dotted;
border-right-style: solid;
border-bottom-style: dotted;
border-left-style: solid;

// left side border
border-left:  6px solid red;  
background-color:  lightgrey;

// Border radius adding rounded curves
border: 2px solid red;
border-radius: 5px;

**margin: 25px 50px 75px 100px;**

-   top margin is 25px
-   right margin is 50px
-   bottom margin is 75px
-   left margin is 100px
# An outline is a line that is drawn around elements, OUTSIDE the borders, to make the element "stand out". Adding border outside border 
  border: 5px solid black;
  outline: #4CAF50 solid 5px;
  outline-color:  red;
  outline-style:  solid; 
  margin: auto;  
  padding: 20px;
  text-align: center;
text-align: center, left, right;
  
```
The  `outline-style`  property specifies the style of the outline, and can have one of the following values:

-   `dotted`  - Defines a dotted outline
-   `dashed`  - Defines a dashed outline
-   `solid`  - Defines a solid outline
-   `double`  - Defines a double outline
-   `groove`  - Defines a 3D grooved outline
-   `ridge`  - Defines a 3D ridged outline
-   `inset`  - Defines a 3D inset outline
-   `outset`  - Defines a 3D outset outline
-   `none`  - Defines no outline
-   `hidden`  - Defines a hidden outline

The  `border-style`  property specifies what kind of border to display.

The following values are allowed:

-   `dotted`  - Defines a dotted border
-   `dashed`  - Defines a dashed border
-   `solid`  - Defines a solid border
-   `double`  - Defines a double border
-   `groove`  - Defines a 3D grooved border. The effect depends on the border-color value
-   `ridge`  - Defines a 3D ridged border. The effect depends on the border-color value
-   `inset`  - Defines a 3D inset border. The effect depends on the border-color value
-   `outset`  - Defines a 3D outset border. The effect depends on the border-color value
-   `none`  - Defines no border
-   `hidden`  - Defines a hidden border


# text-align:  justify;
- When the `text-align` property is set to "justify", each line is stretched so that every line has equal width, and the left and right margins are straight (like in magazines and newspapers)
  ```sh
  border: 1px solid black;
  padding: 10px;
  width: 200px;
  height: 200px;
  text-align: justify;
  ```
# text-transform: uppercase, lowercase, capitalize;

# text-indent: 50px; is used to provider indent like a paragraph initial space

# letter-spacing: 3px; 
# word-spacing: 10px;
# line-height:  1.8;

# The  `text-shadow`  property adds shadow to text.

The following example specifies the position of the horizontal shadow (3px), the position of the vertical shadow (2px) and the color of the shadow (red)
``` text-shadow:  3px 2px red; ```

# Glyphicon
```sh
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
<i class="glyphicon glyphicon-cloud"></i>  
<i class="glyphicon glyphicon-remove"></i>  
<i class="glyphicon glyphicon-user"></i>  
<i class="glyphicon glyphicon-envelope"></i>  
<i class="glyphicon glyphicon-thumbs-up"></i>

```
