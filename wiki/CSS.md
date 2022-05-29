# CSS Tutorial
## 1. CSS Introduction
### 1.1 What is CSS
CSS stands for Cascading Style Sheets

CSS is used to beautify web page and it relies on HTML

The latest version of CSS is `css3`, which can separate the web page from the content and provide precise pixel-level control over the layout and other effects of the elements in the web page.

### 1.2 Why Use CSS
1. Although some HTML tags can be set style, poorly handled details
2. HTML to achieve the style effect will appear a lot of duplicate code, so will become a long and expensive process.

## 2. Basic CSS usage
### 2.1 CSS Syntax
A CSS rule consists of a selector and a declaration block.

![CSS Syntax](https://www.w3schools.com/css/img_selector.gif) 

The selector points to the HTML element you want to style.

The declaration block contains one or more declarations separated by **semicolons**.

Each declaration includes a CSS property name and a value, separated by a colon.

Multiple CSS declarations are separated with **semicolons**, and declaration blocks are surrounded by **curly braces**.

If the property value consists of more than one word, put the value in quotation marks

*Do note add a space between the property value and the unit*

### 2.2 CSS Comments
```CSS
/*comments*/
```

### 2.3 How to Add CSS
#### 2.3.1 External CSS
With an external style sheet, you can change the look of an entire website by changing one file
```HTML
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
```

##### 2.3.1.1 Attribute
- `ref` : Relationship between the current file and the introduced file
- `type` : CSS type
- `href` : Path of linking file

#### 2.3.2 Internal CSS
an internal style sheet may be used if one single html page has a unique style
```HTML
<head>
<style>content</style>
</head>
```


#### 2.3.3 inline CSS
An inline style may be used to apply a unique style for a single element (Higher coupling)
```HTML
<tagName style="property: value; ..."></tagName>
```

#### 2.3.4 CSS Style Priority
If some properties have been defined for the same selector(element ) in different style sheets , the value from the last read style sheet will be used

If the internal style is defined **after** the link to the external style sheet. Internal style will be used, otherwise external style will be used

1. Inline style(inside an HTML element)
2. External and internal style sheets (in the head section)
3. Browser default

## 3. CSS Selectors
### 3.1 Simple selectors
#### 3.1.1 The Universal Selector
The universal selector(*) selects all HTML elements on the page
```CSS
* {
	margin: 0;
	padding: 0;
}
```

#### 3.1.2 The Element Selector
The element selector selects HTML elements based on the element name
```CSS
div {
	width: 100px;
	height: 100px;
}
```

#### 3.1.3 The id Selector
The id selector uses the id attribute of an HTML element to select a specific element

The id of an element is **unique** within a page, so the id selector is used select one **unique** element

To select an element with a specific id, write a hash(`#`) character, followed by the id of the element

```CSS
#para1 {
	text-align: center;
	color: red;
}
```

#### 3.1.4 The class Selector
The class selector selects HTML elements with a specific class attribute

To select elements with a specific class, write a period(`.`) character, followed by the class name

```CSS
.center {
	text-align: center;
	color: red;
}
```

#### 3.1.5 The Grouping Selector
The grouping selector selects all the HTML elements with the same style definition

To Group selectors, separate each selector with a **comma**

```CSS
#div, .cls, p {
	border: 1px solid #0000ff;
}
```

#### 3.1.6 Selectors Priority
Priority (Weight)

id selectors (100) > class selectors (10) > element selectors (1) > universal selectors

The properties in inline style is the max weight (1000)

### 3.2 Combinators
A combinator is something that explains the relationship between the selectors

A combinator can contain more than one simple selector. Between this simple selectors, we can include a combinator

There are four different combinators in CSS:
- descendant selector (space)
- child selector (>)
- adjacent sibling selector (+)
- general sibling selector (~)

#### 3.2.1 Descendant Selector
The descendant selector matches all elements that are descendants of a specified element

```CSS
div p {
	background-color: yellow;
}
```

#### 3.2.2 Child Selector
The child selector selects all elements that are the children of a specified element

```CSS
div > p {
	background-color: yellow;
}
```

#### 3.2.3 Adjacent Sibling Selector
The adjacent sibling selector is used to select an element that is directly after another specific element

Sibling elements must have the same parent element, and "adjacent" means "**immediately following**"

```CSS
div + p {
	background-color: yellow;
}
```

#### 3.2.4 General Sibling Selector
The general sibling selector selects all elements that are **next** sibling of a specified element

```CSS
div ~ p {
	background-color: yellow;
}
```

## 4. Attribute
### 4.1 Background
The CSS background properties are used to add background effects for elements

#### 4.1.1 background-color
The `background-color` property specifies the background color of an element

```CSS
body {
	background-color: lightblue;
}
```

#### 4.1.2 background-image
The `background-image` property sets one or more background images for an element

```CSS
body {
	background-image: url('paper.gif');
}
```

#### 4.1.3 background-repeat
The `background-repeat` property sets if / how a background image will be repeated.

```CSS
body {
	background-image: url(img/logo.jpg);
	background-repeat: no-repeat;
}
```

#### 4.1.4 background-size
The `background-size` property sets the size of background image

```CSS
body {
	background-size: 200px 200px;
}
```

### 4.2 Text
#### 4.2.1 Color
The `color` property is used to set the color of the text. The color is specified by:

- a color name: like `red`
- a HEX value: like `#ff0000`
- an RGB value: like `rgb(255, 0, 0)`

#### 4.2.2 Text Alignment
The `text-align` property specifies the horizontal alignment of text in an element

```CSS
text-align: left | right | center | justify | initial (default) | inherit;
```

#### 4.2.3 Text Decoration
The text-decoration property specifies the decoration added to text, and is a shorthand property for:

- text-decoration-line (required)
- text-decoration-color
- text-decoration-style
- text-decoration-thickness

```CSS
a {
	text-decoration: none;
}
```

#### 4.2.4 Text indentation
The `text-indent` property specifies the indentation of the first line in a text-block.

Unit: `em` (How many are characters in text)

```CSS
p {
	text-indent: 4em;
}
```

### 4.3 Fonts
#### 4.3.1 Font Families
The `font-familiy` property to specify the font of a text

Generic font families:

- `Serif` fonts have a small stroke at the edges of each letter. They create a sense of formality and elegance.
- `Sans-serif` fonts have clean lines (no small strokes attached). They create a modern and minimalistic look.
- `Monospace` fonts - here all the letters have the same fixed width. They create a mechanical look. 
- `Cursive` fonts imitate human handwriting.
- `Fantasy` fonts are decorative/playful fonts. 

```CSS
p {
	font-family: Arial, Helvetica, sans-serif;
}
```

1. If the font name is more than one word, it must be in **quotation** marks
2. The `font-family` property should hold several font names as a "fallback" system, to ensure maximum compatibility between browsers/operating systems. **Start with the font you want**, and **end with a generic family** (to let the browser pick a similar font in the generic family, if no other fonts are available). The font names should be separated with **comma**. 


#### 4.3.2 Font Size
The `font-size` property sets the size of the text

This property has three units:
- `px`
- `em`
- `%`


##### 4.3.2.1 Responsive Font Size
The text size can be set with a `vw` unit, which means the "viewport width".

That way the text size will follow the size of the browser window


#### 4.3.3 Font Style
The font-style property is mostly used to specify italic text

##### 4.3.3.1 Values
- `normal` - The text is shown normally
- `italic` - The text is shown in italics
- `oblique` - The text is "leaning" (oblique is very similar to italic, but less supported)


#### 4.3.4 Font Weight
The `font-weight` property specifies the weight of a font

##### 4.3.4.1 Values
<++>
- `Bold`
- `100-900` : The value is larger and the font is bolder
	- `400` : `normal`
	- `700` : `Bold`


### 4.4 Layout
#### 4.4.1 The display Property
The `display` property specifies if / how an element is displayed

The default display value for most elements is `block` or `inline`

##### 4.4.1.1 Values
- `none` : The element will be hidden
- `block` : can set width and height and also has line break
- `inline` : neither set width and height nor has line break
- `inline-block` : can set width and height but does not have line break

#### 4.4.2 The position Property
The position property specifies the type of positioning method used for an element (static, relative, fixed, absolute or sticky)

There are five different position values:

- `static`
- `relative`
- `fixed`
- `absolute`
- `sticky`

##### 4.4.2.1 position: static
An element with position: static (default); is not positioned in any special way; it is always positioned according to the normal flow of the page

##### 4.4.2.2 position: relative
Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be **adjusted away from its normal position**. Other content will not be adjusted to fit into any gap left by the element.

```CSS
div.relative {
	position: relative;
	left: 30px;
	border: 1px solid red;
}
```

##### 4.4.2.3 position: fixed
An element with `position: fixed`; is positioned relative to the **viewport**, which means it always stays in the same place even if the page is scrolled.

A fixed element does **not leave a gap in the page** where it would normally have been located

##### 4.4.2.4 position: absolute
An element with position: absolute; is positioned relative to the **nearest positioned ancestor**

If an absolute positioned element has no positioned ancestors, it uses the document **body**, and moves along with page scrolling

**Absolute positioned elements are removed from the normal flow, and can overlap elements**
### 4.4.3 Float
#### 4.4.3.1 The float Property
The `float` property is used for positioning and formatting content

The float property can have one of the following values:

- `left` - The element floats to the left of its container
- `right` - The element floats to the right of its container
- `none` - The element does not float (will be displayed just where it occurs in the text). This is default
- `inherit` - The element inherits the float value of its parent

Tips:
1. Only horizontal `float`, no vertical `float`
2. `float` will transfer the display property to `block` 
3. The element after float elements will **surround** the float element (Typical applications are text around images)
4. The element before float elements will no effect (If you want two block elements to be displayed side by side, you must make both block elements `float`)

### 4.4.4 Box Model
The CSS box model is essentially a box that wraps around every HTML element. It consists of: `margin`, `border, ``padding`, and the actual content

![Box Model](https://www.runoob.com/images/box-model.gif) 

Explanation of the different parts:

- `Content` - The content of the box, where text and images appear
- `Padding` - Clears an area around the content. The padding is **transparent**
- `Border` - A border that goes around the padding and content
- `Margin` - Clears an area outside the border. The margin is **transparent**

##### 4.4.4.1 Border
Set all `border` properties
1. Set the width, style, color of the border
```CSS
table, th, td {
	border: 1px solid black;
}
```

2. Use `border-width`, `border-style`, `border-color`, `border-collapse` to separate setting
```CSS
p {
	border-style: dashed;
	border-color: red;
	border-width: 1px;
	border-collapse: collapse | separate;
}
```

3. Order of setting property values: top -> right -> bottom -> left
- Set one property: every side are consistent 
- Set two properties: top and bottom are consistent and also right and left are consistent
- Set three properties: top, right, bottom are not consistent, but right and left are consistent
- Set four properties: any side are not consistent

#### 4.4.4.2 Padding
Padding is used to create space around an element's content, inside of any defined borders

*Padding will change the shape of Box Model therefore less use*

##### 4.4.4.2.1 Padding - Individual Sides
CSS has properties for specifying the padding for each side of an element:


- padding-top
- padding-right
- padding-bottom
- padding-left

All the padding properties can have the following values:
- 
- `length` - specifies a padding in `px`, `pt`, `cm`, etc.
- `%` - specifies a padding in % of the width of the containing element
- `inherit` - specifies that the padding should be inherited from the parent element

##### 4.4.2.2 Padding - Shorthand Property
The padding property is a shorthand property for the following individual padding properties:
 
- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`


#### 4.4.4.3 Margin
The CSS margin properties are used to create space around elements, outside of any defined borders

##### 4.4.4.3.1 Margin - Individual Sides
CSS has properties for specifying the margin for each side of an element:
- 
- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

All the margin properties can have the following values:
- 
- `auto` - the browser calculates the margin
- `length` - specifies a margin in `px`, `pt`, `cm`, etc.
- `%` - specifies a margin in % of the width of the containing element
- `inherit` - specifies that the margin should be inherited from the parent element


