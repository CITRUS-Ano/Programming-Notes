# HTML Tutorial
## 1. Web Programming Design
### 1.1 B/S Architecture
- B: Browse
- S: Server

---

## 2. Basic syntax
HTML: Hypertext markup language

### 2.1 Basic Syntax
#### 2.1.1 Label
- Single label
	- Without attribute: `<labelName />`
	- With attribute: `<labelName propertyName="propertyValue" />` 
- Double label
	- Without attribute: `<labelName></labelName>`  
	- With attribute: `<labelName propertyName="propertyValue"></labelName>`  

#### 2.1.2 Overall Structure
- `<html></html>`: Indicates that it is currently a Web page
- `<head></head>`: Declare header information
- `<body></body>`: body part: can be displayed on a Web page

#### 2.1.3 Doctype
`<!DOCTYPE html>`: html5 version declaration	 **Need to write the first line**

#### 2.1.4 Code
```HTML
<!DOCTYPE html> <!-- html5 version declaration -->
<!--Web page area-->
<html>
     <!--head area -->
    <head>
        <!--indicate the encoding format of html-->
        <meta charset="utf-8" />
        <!--the title of page and also the default name when bookmarking a web page-->
        <title>Basic Syntax</title>
        <!--induct css and js-->
        <link rel="stylesheet" href="the path of css">
        <script src="the path of js" type="text/javascript" charset="utf-8"></script>
    </head>
     <!--content area: can be display in web page -->
    <body>
        hello
    </body>
</html>
```


---


## 3. Common used labels
### 3.1 Title
`<h1></h1>` ~ `<h6></h6>`: the size from big to small

*using multiple h1 label is not suggesting because h1 label can be gotten by search engineer*  

### 3.2 horizon
`<hr />`

##### 3.2.1 properties
- `width`: 1.percentage 2.px
- `align`: `left` / `right` / `center` (default)
- `size`:	number

### 3.3 Paragraph
`<p></p>`: automatically line break

#### 3.3.1 Common properties
- `align`:
	- `left` (default)
	- right
	- center 
	- justify: align the left and right

### 3.4 Line break
`<br />: html don't `identify enter key


### 3.5 List
#### 3.5.1 Unordered list
##### 3.5.1.1 Format
```HTML
<ul>
	<li></li>
	<li></li>
	...
</ul>
```

##### 3.5.1.2 Commonly properties
- `type`: the icon of list 
	- `square`
	- `circle`
	- `disc` (default)

#### 3.5.2 Ordered list
##### 3.5.2.1 Format
```HTML
<ol>
	<li></li>
	<li></li>
	...
</ol>
```

##### 3.5.2.2 Common properties
- `type`: the icon of list 
	- `1`: number sign (default)
	- `a`: lowercase alphabet
	- `A`: uppercase alphabet
	- `i`: lowercase Roman alphabet
	- `I`: uppercase Roman alphabet


### 3.6 Div
`div` is a block element, used for laying out

```HTML
<div>content</div>
```

#### 3.6.1 Commonly properties
- align: the content of div element's align format

### 3.7 Span
`span` is used for combining inline elements in a document

default length is the length of content

```HTML
<span>content</span>
```

### 3.8 Formatted label
#### 3.8.1 font 
`<font></font>`: set the relative font properties (inline elements)

##### 3.8.1.1 Common properties
- color
- size
- face: font style

#### 3.8.2 pre
`<pre></pre>`: define pre-formatted text (keep space and line break in text)

#### 3.8.3 document label
They are all inline elements

- Bold label: `<b></b>` / `<strong></strong>`
-  Italic label: `<i></i>`
- Underline label: `<u></u>`
- Midline label: `<del></del>`
- Subscript label: `<sub></sub>`
- Superscript label: `<sup></sup>`

### 3.9 Hyperlink: a label
`<a>` defines hyperlinks used for jump into another page from current page

`<a>` is an inline element

```HTML
<a href="path or url">content</a>
<a href="#">content</a>		<!-- default current address (refresh) -->
```

#### 3.9.1 Common Properties
- `href` : necessary [label](label)
	- relative path
	- absolute path
	- URL
- `target` : the format of opening window
	- `_self` : current window 
	- `blank` : new window
	- `_parent`  
	- `_top` 

#### 3.9.2 The implementation of anchor points 
`href` can be `#` if want to jump into current page

1. Used by the `name` properties of a label
```HTML
<a name="x"></a>
<a href="#x"></a>
```

2. Used by the `id` properties of other labels
```HTML
<p id="x"></p>
<a href="#x"></a>
```

### 3.10 Image
`img` label is an inline element

#### 3.10.1 Common properties
- necessary properties
	- `src` : the address of image introduced (local or network)
- optional properties
	- `title` : the text when mouse hover the image
	- `alt` : the text when image loads error
	- `width`
	- `height`
	- `border` 
	- `align` 

Jump into another page when image is clicked
```HTML
<a href="url"><img src=""></a>
```

### 3.11 Table
#### 3.11.1 label
- `<table></table>` : define a HTML table
- `<tr></tr>` : define a row, tr element includes single or multiple `th` or `td` elements
- `<td></td>` : define a standard cell
- `<th></th>` : define a cell at the table header (title)

The text in `th` element display bold text while `td` element is the left align text

#### 3.11.2 Table properties
- `border` 
- `width` : pixels or percentage 
	- The percentage refers to the width of the parent element, if not set, refers to the width of screen
- `height`  
	- The percentage refers to the width of the parent element, if not set, refers to the width of screen
- `align`

CSS style: `border-collapse: collapse;`	combine table border

#### 3.11.2 tr properties
- `align` : horizontal alignment
- `valign` : vertical alignment
	- `top` / `middle` / `buttom`
- `bgcolor` : set the row color of table

#### 3.11.3 Combine cells
`<td>` : `colspan` and `rowspan` declare the combination of the number of rows or columns

- `rowspan` : vertical combination
- `colspan` : horizontal combination

```HTML
<td rowspan="2"></td>
<td colspan="2"></td>
```

### 3.12 Form
<++>
