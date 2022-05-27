# HTML Tutorial
## 1. Web Programming Design
### 1.1 B/S Architecture
- B: Browse
- S: Server

---

## 2. Basic syntax
HTML: Hypertext markup language

### 2.1 Basic Syntax
#### 2.1.1 tag
- Single tag
	- Without attribute: `<tagName />`
	- With attribute: `<tagName propertyName="propertyValue" />` 
- Double tag
	- Without attribute: `<tagName></tagName>`  
	- With attribute: `<tagName propertyName="propertyValue"></tagName>`  

#### 2.1.2 Overall Structure
- `<html></html>`: Indicates that it is currently a Web page
- `<head></head>`: Declare header information
- `<body></body>`: body part: can be displayed on a Web page

#### 2.1.3 `Doctype`
`<!DOCTYPE html>`: `html5` version declaration	 **Need to write the first line**

#### 2.1.4 Code
```HTML
<!DOCTYPE html> <!--  version declaration -->
<!--Web page area-->
<html>
     <!--head area -->
    <head>
        <!--indicate the encoding format of html-->
        <meta charset="utf-8" />
        <!--the title of page and also the default name when bookmarking a web page-->
        <title>Basic Syntax</title>
        <!--induct CSS and JavaScript-->
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


## 3. Common used tags
### 3.0 Attribute values that are common to all tags
- `id` : Used to identify the uniqueness of an element
- `name` : Parameter name of submitted data
- `style` : Set inline style of element
- `class` : Set style name of element

### 3.1 Headings
`<h1></h1>` ~ `<h6></h6>`: the size from big to small

*using multiple `h1` tag is not suggesting because `h1` tag can be gotten by search engineer*  

### 3.2 Horizon
`<hr />`

##### 3.2.1 Attribute
- `width`: 1.percentage 2.`px`
- `align`: `left` / `right` / `center` (default)
- `size`:	number

### 3.3 Paragraph
`<p></p>`: automatically line breaks

#### 3.3.1 Attribute
- `align`:
	- `left` (default)
	- `right`
	- `center` 
	- `justify`: align the left and right

#### 3.4 Line breaks
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

##### 3.5.1.2 Attribute
- `type`: the icon of list 
	- `square`
	- `circle`
	- `disc` (default)

#### 3.5.2 Ordered list
##### 3.5.2.1 Formatting
```HTML
<ol>
	<li></li>
	<li></li>
	...
</ol>
```

##### 3.5.2.2 Attribute
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

#### 3.6.1 Attribute
- align: the content of div element's align format

### 3.7 Span
`span` is used for combining inline elements in a document

Default length is the length of content

```HTML
<span>content</span>
```

### 3.8 Formatted tag
#### 3.8.1 font 
`<font></font>`: set the relative font attribute (inline elements)

##### 3.8.1.1 Attribute
- color
- size
- face: font style

#### 3.8.2 pre
`<pre></pre>`: define pre-formatted text (keep space and line breaks in text)

#### 3.8.3 document tag
They are all inline elements

- Bold tag: `<b></b>` / `<strong></strong>`
-  Italic tag: `<i></i>`
- Underline tag: `<u></u>`
- Midline tag: `<del></del>`
- Subscript tag: `<sub></sub>`
- Superscript tag: `<sup></sup>`

### 3.9 Hyperlink: a tag
`<a>` defines hyperlinks used for jump into another page from current page

`<a>` is an inline element

```HTML
<a href="path or url">content</a>
<a href="#">content</a>		<!-- default current address (refresh) -->
```

#### 3.9.1 Attribute
- `href` : necessary [tag](tag)
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

1. Used by the `name` attribute of a tag
```HTML
<a name="x"></a>
<a href="#x"></a>
```

2. Used by the `id` attribute of other tags
```HTML
<p id="x"></p>
<a href="#x"></a>
```

### 3.10 Image
`img` tag is an inline element

#### 3.10.1 Attribute
- necessary attribute
	- `src` : the address of image introduced (local or network)
- optional attribute
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

---



### 3.11 Table
#### 3.11.1 Tag
- `<table></table>` : define a HTML table
- `<tr></tr>` : define a row, tr element includes single or multiple `th` or `td` elements
- `<td></td>` : define a standard cell
- `<th></th>` : define a cell at the table header (title)

The text in `th` element display bold text while `td` element is the left align text

#### 3.11.2 Table attribute
- `border` 
- `width` : pixels or percentage 
	- The percentage refers to the width of the parent element, if not set, refers to the width of screen
- `height`  
	- The percentage refers to the width of the parent element, if not set, refers to the width of screen
- `align`

CSS style: `border-collapse: collapse;`	combine table border

#### 3.11.3 `tr` Attribute
- `align` : horizontal alignment
- `valign` : vertical alignment
	- `top` / `middle` / `buttom`
- `bgcolor` : set the row color of table

#### 3.11.4 Combine cells
`<td>` : `colspan` and `rowspan` declare the combination of the number of rows or columns

- `rowspan` : vertical combination
- `colspan` : horizontal combination

```HTML
<td rowspan="2"></td>
<td colspan="2"></td>
```

---



### 3.12 Form
#### 3.12.1 form
`<form>` is used to create forms for user input

`form` can include input element (text fields, radio boxes, check boxes, submit buttons, etc), and also can include `textarea` etc

`form` is a block element. It is used to transfer data to the server

*When the form is submitted, the value of the name attribute of the single element must be set, otherwise the data cannot be retrieved*

##### 3.12.1.1 Attribute
- `action` : Address for form submission
- `method` : Submission method (Not case-sensitive)
	- `GET`  (default)
	- `POST` 
- `target` : The way to open the window when submitting data
	- `_self` 
	- `_blank` 

##### 3.12.1.2 The difference between get request and post request
1. `Post` requests require server support
2. The parameters of the `get` request are followed by the browser address while the `post` request is not (post request will store data in **request body**)
3. `Get` requests are less secure than `post` requests
4. There is a limit to the length of the data passed in a `get` request, while there is basically no limit on `post` requests (The limited length of `post` request refers to server)
5. `Get` requests are faster than `post` request, about twice at much
6. `Get` request have cache and will store the data in the browser ( i.e. on local disk ) while `post`  requests have no cache

#### 3.12.2 input
`<input>` : For collecting user information (inline element)

Input text has several styles depending on the value of type attribute (e.g. text fields, radio boxes, check boxes, submit buttons, etc)

##### 3.12.2.1 Attribute 
- `type`: types of element
	- `text`  
	- `password`
	- `radio` : radio box 
		- radio / check boxes require` name` attribute to set a group
	- `checkbox` : check boxes
	- `file` : Upload a file ()
		- if the form is for uploading files, it needs to set a property: `enctype="nultipart/form-data"` and select `post` submission method
	- `hidden` : Pass the data but can't be displayed
	- three button
		- `button`
		- `submit`
		- `reset` *: only can clear text you input*
	- `date` 
- `value` 
- `readonly`
- `maxlength` 
- `disabled` : Disable the current tag
- `name` : name is necessary to submit this tag's data

### 3.12.3 `Textarea`
`<textarea></textarea>` defines a multi-line input control(text area)

The size of a `<textarea>` is specified by the `<cols>` and `<rows>` attributes (or with CSS)

#### 3.12.3.1 Attribute
- `cols` : the number of columns (Width)
- `rows` : the number of rows (Height)


### 3.12.4 label
`<label>` tag used for several `input` element defining marking

`label` can focus on the element

#### 3.12.4.1 Attribute
- `for` : Specifies the `id` of the form element the label should be bound to

### 3.12.4 Button
`<button>content</button>`

Content can be text, images etc

#### 3.12.4.1 Attribute
- `type`
	- `button`
	- `submit` : (default)
	- `reset`

#### 3.12.5 Drop-down list
The `<select>` element is used to create a drop-down list (inline element)
The `<option>` tags inside the `<select>` element define the available options in the drop-down list

#### 3.12.5.1 Attribute
1. `select` attribute
	- `multiple` : Specifies that multiple option can be selected at once
	- `size` : Defines the number of visible options in a drop-down list
2. `option` attribute
	- `selected` : default option selected
	- `value` : the value of option submitted to server
		-	if set the attribute of value, will submit the value
		- if not set the attribute of value, will submit the text value in option double tag

---


### 3.13 Character entity
Some characters are reserved in HTML, reserved characters must be replaced with **character entities**

#### 3.13.1 Useful Character Entities
- `$lt;` : `<`
- `&gt;` : `>`
- `&nbsp;` : `<SPACE>`
- `&copy; `: `©️` (copyright notice)

### 3.14 Classification of tags
There are three display values: `block`, `inline`, `inline block`

#### 3.14.1 Block-level Elements
A block-level element always starts on a new line, and the browsers automatically add some space (a margin) before and after the element

A block-level element always takes up the full width available. It is the 100% of its parent element unless a width  is defined

Two commonly used block elements are: `<p>` and `<div>`
- The `<p>` element defines a paragraph in an HTML document
- The `<div>` element defines a division or a section in an HTML document

#### 3.14.2 Inline Elements
An inline element only takes up as much width as necessary
- `<span>`

#### 3.14.2 Inline-block Elements
An inline-block element does not start on a new line, but it can be set width and Height

