# Demo 8
# CSS Counters

 - CSS counters are like "variables". The variable values can be incremented by CSS rules
 - To use a CSS counter, it must first be created with `counter-reset`
-   
```sh
body {
  counter-reset: sai; // Creates or resets a counter
}

h2::before {
  counter-increment: sai; // Increments a counter value
  content: "Section " counter(sai) ": "; // Inserts generated content
  // `counter()` or `counters()` function - Adds the value of a counter to an element
}
```
- **Nesting Counters** creating contents on Page
```sh
<!DOCTYPE html>
<html>
<head>
<style>
body {
  counter-reset: section;
}

h1 {
  counter-reset: subsection;
}

h1::before {
  counter-increment: section;
  content: "Section " counter(section) ". ";
}

h2::before {
  counter-increment: subsection;
  content: counter(section) "." counter(subsection) " ";
}
</style>
</head>
<body>


<h1>HTML tutorials:</h1>
<h2>HTML Tutorial</h2>
<h2>CSS Tutorial</h2>

<h1>Scripting tutorials:</h1>
<h2>JavaScript</h2>
<h2>VBScript</h2>

<h1>XML tutorials:</h1>
<h2>XML</h2>
<h2>XSL</h2>

<p><b>Note:</b> IE8 supports these properties only if a !DOCTYPE is specified.</p>

</body>
</html>
```

# Specificity Hierarchy

Every selector has its place in the specificity hierarchy. There are four categories which define the specificity level of a selector:

**Inline styles** - An inline style is attached directly to the element to be styled. Example: `<h1 style="color: #ffffff;">.`

**IDs** - An ID is a unique identifier for the page elements, such as #navbar.

**Classes, attributes and pseudo-classes** - This category includes .classes, [attributes] and pseudo-classes such as :hover, :focus etc.

**Elements and pseudo-elements** - This category includes element names and pseudo-elements, such as h1, div, :before and :after.

# CSS Gradients

 - CSS gradients let you display smooth transitions between two or more specified colors.
 - CSS defines two types of gradients:
	  -   **Linear Gradients (goes down/up/left/right/diagonally)**
	  -   **Radial Gradients (defined by their center)**
 - **CSS Linear Gradients**
	  - `background-image: linear-gradient(direction, color-stop1, color-stop2, ...);`
	  - To create a linear gradient you must define at least two color stops. 
	  - Color stops are the colors you want to render smooth transitions among. 
	  - You can also set a starting point
	  - Direction (or an angle) along with the gradient effect.
	  - **Linear Gradient - Left to Right** `background-image: linear-gradient(to right, red , yellow);`
	  - **Linear Gradient - Diagonal** `background-image: linear-gradient(to bottom right, red, yellow);`
	  - **Using Angles** `background-image: linear-gradient(-90deg, red, yellow);`
	  - **Using Multiple Color Stops** `background-image: linear-gradient(red, yellow, green, blue);`
	  - **Using Transparency** `background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));`
 - **CSS Radial Gradients**

	  - A radial gradient is defined by its center.

	- To create a radial gradient you must also define at least two color stops.
	- `background-image: radial-gradient(shape size at position, start-color, ..., last-color);`
	- By default, shape is ellipse, size is farthest-corner, and position is center.
	- **Radial Gradient - Evenly Spaced Color Stops (this is default)** `background-image: radial-gradient(red, yellow, green);`
	- **Radial Gradient - Differently Spaced Color Stops** `background-image: radial-gradient(red 5%, yellow 15%, green 60%);`
	- **Set Shape** `background-image: radial-gradient(circle, red, yellow, green);` Eclipse is default

# CSS Shadow Effects
 - `text-shadow: 2px 2px 5px(blur) red;`
 - The CSS `box-shadow` property applies shadow to elements.
 - `box-shadow: 10px 10px 10px rgba(0, 0, 0, .5);`
# CSS white-space Property
- The `white-space` property specifies how white-space inside an element is handled.

| Element | Uses |
|--|--|
|**normal** | Sequences of whitespace will collapse into a single whitespace. Text will wrap when necessary. This is default |
| **nowrap** | Sequences of whitespace will collapse into a single whitespace. Text will never wrap to the next line. The text continues on the same line until a <br> tag is encountered |
| **pre** |  Whitespace is preserved by the browser. Text will only wrap on line breaks. Acts like the `<pre>` tag in HTML |
| pre-line | Sequences of whitespace will collapse into a single whitespace. Text will wrap when necessary, and on line breaks
| pre-wrap | Whitespace is preserved by the browser. Text will wrap when necessary, and on line breaks |

# CSS Text Overflow
- The CSS `text-overflow` property specifies how overflowed content that is not displayed should be signaled to the user.
```sh
p.test1 {
  white-space: nowrap; // comes text in single line
  width: 200px; 
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: clip; // clipped
}

p.test2 {
  white-space: nowrap; 
  width: 200px; 
  border: 1px solid #000000;
  overflow: hidden;
  text-overflow: ellipsis;// (...)
}
```

# CSS Word Wrapping
The CSS `word-wrap` property allows long words to be able to be broken and wrap onto the next line.

    width: 100px; 
    border: 1px solid #000000;
    word-wrap: break-word;
# CSS Word Breaking
The CSS `word-break` property specifies line breaking rules.

    p.test1 {  
      width: 140px; 
      border: 1px solid #000000;
      word-break: keep-all;  // this will take text to next line without breaking
    }  
      
    p.test2 {
      width: 140px; 
      border: 1px solid #000000;
      word-break: break-all;  // this will break text and displays remaining text in next line
    }

# CSS Writing Mode
The CSS `writing-mode` property specifies whether lines of text are laid out horizontally or vertically.
```
writing-mode: horizontal-tb; // Default horizontal
writing-mode: vertical-lr; // vertical text displaying
```

# CSS 2D Transforms
CSS transforms allow you to move, rotate, scale, and skew elements.

With the CSS `transform` property you can use the following 2D transformation methods:
-   `translate()` 
	- moves an element from its current position (according to the parameters given for the X-axis and the Y-axis).
	- `transform: translate(50px, 100px);`
-   `rotate()`
	- rotates an element clockwise or counter-clockwise according to a given degree.
	- `transform: rotate(20deg);`
-   `scale()`
	- The `scale()` method increases or decreases the size of an element (according to the parameters given for the width and height).
	- `transform: scale(2, 3);`
	- `transform: scale(0.5, 0.5);` decreases the element to be half of its original width and height
-   `scaleX()`
	- The `scaleX()` method increases or decreases the width of an element.
	- `transform: scaleX(2);` increases the element to be two times of its original width
-   `scaleY()`
	- The `scaleY()` method increases or decreases the height of an element.
-   `skewX()`
	- The `skewX()` method skews(makes some kind of rectange to bend) an element along the X-axis by the given angle.
	- `transform: skewX(20deg);`
-   `skewY()`
-   `skew()`
	- `transform: skew(20deg, 10deg);`
-   `matrix()`
	- The `matrix()` method combines all the 2D transform methods into one.
	- The matrix() method take six parameters, which allows you to rotate, scale, move (translate), and skew elements.
	- The parameters are as follow: matrix(scaleX(),skewY(),skewX(),scaleY(),translateX(),translateY())
	- transform: matrix(1, -0.3, 0, 1, 0, 0);
# CSS 3D Transforms Methods
- With the CSS `transform` property you can use the following 3D transformation methods:
	-   `rotateX()`
		- rotates an element around its X-axis at a given degree(it rotates in front direction in X-axis)
		- `transform: rotateX(150deg);`
	-   `rotateY()`
		- rotates an element around its Y-axis at a given degree(it rotates in front direction in Y-axis)
	-   `rotateZ()`
		- rotates an element around its Z-axis at a given degree (rotates the div in circular direction)
# CSS Transitions
CSS transitions allows you to change property values smoothly, over a given duration.

How to Use CSS Transitions?
- To create a transition effect, you must specify two things:
	-   the CSS property you want to add an effect to
	-   the duration of the effect
	 ```sh 
		div {  
			width: 100px;  
			height: 100px;  
			background: red;  
			transition: width 2s;//Now width here will be 100px  
		} 
		```
- The transition effect will start when the specified CSS property (width) ****changes** value**.
	```sh
	div:hover {  
	    width: 300px;
	}
	```
- Notice that when the cursor mouses out of the element, it will gradually change back to its original style.
## Change Several Property Values
```sh
div {
  width: 100px;
  height: 100px;
  background: red;
  -webkit-transition: width 2s, height 4s; /* For Safari 3.1 to 6.0 */
  transition: width 2s, height 4s;
}

div:hover {
  width: 300px;
  height: 300px;
}
```
## Specify the Speed Curve of the Transition

The `transition-timing-function` property specifies the speed curve of the transition effect.

The transition-timing-function property can have the following values:

-   `ease` - specifies a transition effect with a slow start, then fast, then end slowly (this is default)
	- `transition-timing-function: linear;`
-   `linear` - specifies a transition effect with the same speed from start to end
-   `ease-in` - specifies a transition effect with a slow start
-   `ease-out` - specifies a transition effect with a slow end
-   `ease-in-out` - specifies a transition effect with a slow start and end
-   `cubic-bezier(n,n,n,n)` - lets you define your own values in a cubic-bezier function
## Delay the Transition Effect
The `transition-delay` property specifies a delay (in seconds) for the transition effect.

    transition-delay: 1s;

# Transition + Transformation

    div {
      width: 100px;
      height: 100px;
      background: red;
      transition: width 2s, height 2s, transform 2s;
    }
    
    div:hover {
      width: 300px;
      height: 300px;
      transform: rotate(180deg);
    }
# Shorthand
```sh
transition-property: width;  
transition-duration: 2s;  
transition-timing-function: linear;  
transition-delay: 1s;
```

    transition: width 2s linear 1s;


# CSS Animations

 - An animation lets an element gradually change from one style to another.
 - To use CSS animation, you must first specify some keyframes for the animation.
	 - Keyframes hold what styles the element will have at certain times.
 ```sh
 /* The animation code */  
@keyframes example {  
	from {background-color: red;}  
	to {background-color: yellow;}  
}  
  
/* The element to apply the animation to */  
div {  
	width: 100px;  
	height: 100px;  
	background-color: red;  
	animation-name: example;  
	animation-duration: 4s;  // this effect will be there for 4sec
}
 ```
 - In the example above we have specified when the style will change by using the keywords "from" and "to" (which represents 0% (start) and 100% (complete)).
 - It is also possible to use percent. By using percent, you can add as many style changes as you like.
	 ```sh
		@keyframes example {  
			0% {background-color: red;}  
			25% {background-color: yellow;}  
			50% {background-color: blue;}  
			100% {background-color: green;}  
		}  
		  
		/* The element to apply the animation to */  
		div {  
			width: 100px;  
			height: 100px;  
			background-color: red;  
			animation-name: example;  
			animation-duration: 4s;  
		}
		```
- Applying extra properties
	```sh
	/* The animation code */  
	@keyframes example {  
		0% {background-color:red; left:0px; top:0px;}  
		25% {background-color:yellow; left:200px; top:0px;}  
		50% {background-color:blue; left:200px; top:200px;}  
		75% {background-color:green; left:0px; top:200px;}  
		100% {background-color:red; left:0px; top:0px;}  
	}  
	  
	/* The element to apply the animation to */  
	div {  
		width: 100px;  
		height: 100px;  
		position: relative;  
		background-color: red;  
		animation-name: example;  
		animation-duration: 4s;  
	}
- ## Delay an Animation
	- The `animation-delay` property specifies a delay for the start of an animation.
	- `animation-delay: 2s;`
- ## Set How Many Times an Animation Should Run
	- The `animation-iteration-count` property specifies the number of times an animation should run.
	- `animation-iteration-count: 3;`
	- `animation-iteration-count: infinite;` make the animation continue for ever
- ## Run Animation in Reverse Direction or Alternate Cycles

	The `animation-direction` property specifies whether an animation should be played forwards, backwards or in alternate cycles.

	The animation-direction property can have the following values:

	-   `normal` - The animation is played as normal (forwards). This is default
	-   `reverse` - The animation is played in reverse direction (backwards)
	-   `alternate` - The animation is played forwards first, then backwards
	-   `alternate-reverse` - The animation is played backwards first, then forwards

- ## Specify the Speed Curve of the Animation

	The `animation-timing-function` property specifies the speed curve of the animation.

	The animation-timing-function property can have the following values:

	-   `ease` - Specifies an animation with a slow start, then fast, then end slowly (this is default)
	-   `linear` - Specifies an animation with the same speed from start to end
	-   `ease-in` - Specifies an animation with a slow start
	-   `ease-out` - Specifies an animation with a slow end
	-   `ease-in-out` - Specifies an animation with a slow start and end
	-   `cubic-bezier(n,n,n,n)` - Lets you define your own values in a cubic-bezier function

# Button Stylings
	https://www.w3schools.com/css/css3_buttons.asp
