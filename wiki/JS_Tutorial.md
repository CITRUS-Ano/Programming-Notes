# JS Tutorial

---

## JS Introduction

### JavaScript Can Change HTML Content

```javascript
document.getElementById('demo').innerHTML = 'Hello JavaScript';
```



### JavaScript Can Change HTML Attribute Values

```html
<button onclick="document.getElementById('myImage').src='pic_bulbon.gif'">
	Turn on the light
</button>
```



### JavaScript Can Change HTML Style(CSS)

```java
document.getElementById("demo").style.fontSize = "35px";
```



### JavaScript Can Hide HTML Elements

```javascript
 document.getElementById("demo").style.display = "none";
```



### JavaScript Can Show HTML Elements

```javascript
document.getElementById("demo").style.display = "block";
```



---

## JS Where To

### The `<script>` Tag

```html
<script>
document.getElementById("demo").innerHTML = "My First JavaScript";
</script>
```



### JavaScript Functions and Events

A JavaScript `function` is a block of JavaScript code, that can be executed when "called" for.

*a function can be called when an **event** occurs, like when the user clicks a button.*



### JavaScript in `<head> ` or ` <body>`

Scripts can be placed in the `<body>`, or in the `<head>` section of an HTML page, or in both.



#### JavaScript in `<head>`

```html
<!DOCTYPE html>
<html>
<head>
<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>
</head>
<body>
<h2>Demo JavaScript in Head</h2>

<p id="demo">A Paragraph</p>
<button type="button" onclick="myFunction()">Try it</button>

</body>
</html>
```



#### JavaScript in `<body>`

```html
<!DOCTYPE html>
<html>
<body>

<h2>Demo JavaScript in Body</h2>

<p id="demo">A Paragraph</p>

<button type="button" onclick="myFunction()">Try it</button>

<script>
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
}
</script>

</body>
</html>
```


### Extra JavaScript

External scripts are practical when the same code is used in many different web pages.

**External file: myScript.js**

```javascript
function myFunction() {
  document.getElementById("demo").innerHTML = "Paragraph changed.";
 }
```

To use an external script, put the name of the script file in the `src` (source) attribute of a `<script>` tag:
```html
<script src="myScript1.js"></script>
<script src="myScript2.js"></script>
```



### External References

An external script can be referenced in 3 different ways:

- With a full URL (a full web address)
- With a file path (like /js/)
- Without any path

This example uses a **full URL** to link to myScript.js:

```html
<script src="https://www.w3schools.com/js/myScript.js"></script>
```

This example uses a **file path** to link to myScript.js:

```html
<script src="/js/myScript.js"></script>
```



---

## JS Output

### JavaScript Display Possibilities

JavaScript can "display" data in different ways:

- Writing into an **HTML element**, using `innerHTML`.
- Writing into the **HTML output**using `document.write()`.
- Writing into an **alert box **, using `window.alert()`.
- Writing into the **browser console **, using `console.log()`.

### Using innerHTML
To access an HTML element, JavaScript can use the document.getElementById(id) method.

The id attribute defines the HTML element. The innerHTML property defines the HTML content:

``` JavaScript
document.getElementById("demo").innerHTML = 5 + 6;
```

### Using document.write()
For testing purposes, it is convenient to use document.write():

```JavaScript
document.write(5 + 6);
```

*Using document.write() after an HTML document is loaded, will delete all existing HTML:* 

### Using window.alert()
You can use an alert box to display data:
```JavaScript
// you can skip the `window` keyword
window.alert(5 + 6);
alert(5 + 6);
```

### Using console.log()
```JavaScript
console.log(5 + 6)
```

### JavaScript Print
JavaScript does not have any print object or print methods.

The only exception is that you can call the `window.print()` method in the browser to print the content of the current window.

```html
<button onclick="window.print()">Print this page</button>
```

---

## JavaScript Statements
### JavaScript Programs
In a programming language, these programming instructions are called statements.

*In HTML, JavaScript programs are executed by the web browser.* 

### JavaScript Statements
JavaScript statements are composed of: Values, Operations, Expressions, Keywords and Comments.

### Semicolons ;
Semicolons separate JavaScript statements.

#### Examples
```JavaScript
let a, b, c;  // Declare 3 variables
a = 5;        // Assign the value 5 to a
b = 6;        // Assign the value 6 to b
c = a + b;    // Assign the sum of a and b to c
```

### JavaScript White Space
JavaScript ignores multiple spaces. You can add white space to your script to make it more readable.

### JavaScript Line Length and Line Breaks
For best readability, programmers often like to avoid code lines longer than 80 characters.

If a JavaScript statement does not fit on one line, the best place to break it is after an operator:

#### Examples
```JavaScript
document.getElementById("demo").innerHTML =
"Hello Dolly!";
```

### JavaScript Code Blocks
JavaScript statements can be grouped together in code blocks, inside curly brackets {...}.

### Examples
```JavaScript
function myFunction() {
  document.getElementById("demo1").innerHTML = "Hello Dolly!";
  document.getElementById("demo2").innerHTML = "How are you?";
}
```

### JavaScript Keyword
JavaScript keywords are reserved words. Reserved words cannot be used as names for variables.

| Keyword  | Description                                                  |
|----------|--------------------------------------------------------------|
| var      | Declares a variable                                          |
| let      | Declares a block variable                                    |
| const    | Declares a block constant                                    |
| if       | Marks a block of statemens to be executed on a condition     |
| switch   | Marks a block of statements to be executed in different case |
| for      | Marks a block of statements to be executed in a loop         |
| function | Declares a function                                          |
| return   | Exits a function                                             |
| try      | Implements error handing to a block of statemens             |


## JavaScript Syntax
### JavaScript Values
The JavaScript syntax defines two types of values:
- Fixed values (called **Literals**)
- Variable values (called **Variables**)


### JavaScript Literals
The two most important syntax rules for fixed values are:
1. **Numbers** are written with or without decimals:
```JavaScript
10.50

1001
```

2. String are text, written within double or single quotes:
```JavaScript
"John Doe"

'John Doe'
```

### JavaScript Variables
JavaScript uses the keywords `var`, `let` and `const` to declare variables.

An equal sign is used to assign values to variables.

```JavaScript
let x;
x = 6;
```

### JavaScript Operators
JavaScript uses **arithmetic operators** (`+ `-` ``*` `/`) to compute values:
```JavaScript
(5 + 6) * 10
```

JavaScript uses an **assignment operator** (`=`) to **assign** values to variables.
```JavaScript
let x, y;
x = 5;
y = 6;
```

### JavaScript Expressions
An expression is a combination of values, variables, and operators, which computes to a value.

The computation is called an **evaluation**.
```JavaScript
5 * 10
x * 10
"John" + " " + "Doe"
```

### JavaScript Keyword
JavaScript **Keywords** are used to identify actions to be performed.

The `let` keyword tells the browser to create variables:
```JavaScript
x = 5 + 6;
y = x * 10;
```

The `var` keyword also tells the browser to create variables:
```JavaScript
var x, y;
x = 5 + 6;
y = x * 10;
```

### JavaScript Comments
Code after double slashes `//` or between `/*` and `*/` is treated as a **comment.**
```JavaScript
let x = 5;	// I will be executed

// x = 6;	I will NOT be executed
```

### JavaScript Identifiers / Names
A JavaScript name must begin with:

- A letter (A - Z or a - z) 
- A dollar sign ($)
- Or an underscore(_)

Subsequent characters may be letters, digits, underscores, dollar signs.

### JavaScript is Case Sensitive
All JavaScript identifiers are **case sensitive**.
```JavaScript
let lastname, lastName;
lastName = "Doe";
lastname = "Peterson"
```

*JavaScript does not interpret **LET** or **Let** as the keyword `let`*. 

### JavaScript and Camel Case
Hyphens are not allowed in JavaScript. They are reserved for subtraction.

#### Underscore:
first_name, last_name, master_card, inter_city.

#### Upper Camel Case (Pascal Case):
FirstName, LastName, MasterCard, InterCity.

#### Lower Camel Case:
JavaScript programmers tend to use camel case that **starts with a lowercase letter**:

firstName, lastName, masterCard, interCity.


### JavaScript Character Set
JavaScript uses the **Unicode** character set.

---


## JavaScript Variables
variables are containers for storing values.

#### 4 ways to Declare a JavaScript Variable:
- using `var` 
- using `let`
- using `const` 
- Using nothing

### When to Use JavaScript var?
Always declare JavaScript variables with `var`,`let`, or `const`.

The `var` keyword is used in all JavaScript code from 1995 to 2015.

The `let` and `const` keywords were added to JavaScript in 2015.

If you want your code to run in older browser, you must use `var`.


### When to Use JavaScript const?
If you want a general rule: always declare variables with `const`.

If you think the value of the variable can change, use `let`.


### JavaScript Identifiers
All JavaScript variables must be **identified** with **unique names**.

These unique names are called **identifiers**.

### Declaring a JavaScript Variable
Creating a variable in JavaScript is called "declaring" a variable.

You declare a JavaScript variable with the `var` or the `let` keyword.

After the declaration, the variable has no value (technically it is `undefined`)

To **assign** a value to the variable, use the **equal sign**.

You can also assign a value to the variable when you declare it.

### One Statement, Many Variables
Start the statement with `let` and separate the variables by **comma**.

#### Example
```JavaScript
let person = "John Doe", carName = "Volvo", price = 200;
```

### Value = Undefined 
A variable declared without a value will have the value `undefined`.

### Re-Declaring JavaScript Variables
If you re-declare a JavaScript variable declared with `var`, it will not lose its value.

#### Example
```JavaScript
var carName = "Volvo";
var carName;	// carName will still equal to "Volvo"
```

**You cannot re-declare a variable declared with `let` or `const`**

### JavaScript Arithmetic
If you put a number in quotes, the rest of the numbers will be treated as strings, and concatenated.

#### Example
```JavaScript
let x = 2 + 3 + "5";	// the result of the equation is "55"
```

### JavaScript Dollar Sign $
Since JavaScript treats a dollar sign as a letter, identifiers containing $ are valid variable names.

[Using](Using) the dollar is not very common in JavaScript, but professional programmers often use it as an **alias** for the **main function in JavaScript library**.

In the JavaScript library jQuery, for instance, the main function `$` is used to select HTML elements. In jQuery `$("p");` means "select all p elements". 

### JavaScript Underscore (_)
Since JavaScript treats underscore as a letter, identifiers containing _ are valid variable names.

Using the underscore is not very common in JavaScript, but a convention among professional programmers is to use it as an **alias** for **"private (hidden) variables"**.

---

## JavaScript Let
- Variables defined with `let` cannot be Redeclared.	*With `var` you can*
- Variables defined with `let` must be Declared before use.
- Variable defined with `let` have Block Scope.

### Block Scope
`let` and `const` two keyword provide **Block scope** in JavaScript.

Variables declared inside a {} block cannot be accessed from outside the block.

#### Example
```JavaScript
{
	let x = 2;
}
// x can NOT be used here
```

*Variable declared with `var` keyword can NOT have block scope.*

*Variable declared inside a {}* block can be accessed from outside the block. 

#### Example
```JavaScript
{
	var x = 2;
}
// x CAN be used here
```


### Redeclaring Variables
Redeclaring a variable using the `var` keyword can impose problems.

Redeclaring a variable inside a block will also redeclare the variable outside the block.

#### Example
```JavaScript
var x = 10
// Here x is 10

{
	var x = 2;
	// Here x is 2
}

// Here x is 2
```

Redeclaring a variable using the `let` keyword can solve this problem.

Redeclaring a variable inside a block will not redeclare the variable outside the block.

#### Example
```JavaScript
let x = 10;
// Here x is 10

{
	let x = 2;
	// Here x is 2
}

// Here x is 10
```

### Browser Support
The `let` keyword is not fully supported in Internet Explorer 11 or earlier.

### Redeclaring
Redeclaring a JavaScript variable with `var` is allowed anywhere in a program.

#### Example
```JavaScript
var x = 2;
// Now x is 2

var x = 3;
// Now x is 3
```

With `let` redeclaring a variable in same block is NOT allowed.

#### Example
```JavaScript
var x = 2;	// Allowed
let x = 3;	// Not allowed

{
	let x = 2;	// Allowed
	let x = 3;	// Not allowed
}

{
	let x = 2;	// Allowed
	var x = 3;	// Not Allowed
}
```

Redeclaring a variable with `let`, in another block, IS allowed.

### Let Hoisting
Variables defined with `var` are **hoisted** to the top and can be initialized at any time.

*Meaning: you can use the variable before it is declared.*

#### Example
```JavaScript
// This is OK
carName = "Volvo";
var carName;
```

Variables defined with `let` are also hoisted to the top of the block, but not initialized.

*Meaning: Using a `let` variable before it is declared will result in a `ReferenceError`*

---

## JavaScript Const
Variables defined with `const` cannot be Redeclared.

Variables defined with `const` cannot be Reassigned.

Variable defined with `const` have Block Scope.

### Cannot be Reassigned
A `const` variable cannot be reassigned.

#### Example
```JavaScript
const PI = 3.141592653589793;
PI = 3.14;      // This will give an error
PI = PI + 10;   // This will also give an error
```

### Must be Assigned
JavaScript `const` variables must be assigned a value when they are declared.

### When to use JavaScript const?
- A new Array
- A new Object
- A new Function
- A new RegExp

### Constant Objects and Array
`const` does not define a constant value. It defines a constant reference to a value.

Because of this you can NOT:
- Reassign a constant value
- Reassign a constant array
- Reassign a constant object

But you CAN:
- Change the elements of constant array
- Change the properties of constant object

### Constant Array
#### Example
```JavaScript
// You can create a constant array:
const cars = ["saab", "Volvo", "BMW"];

// You can change an element:
cars[0] = "Toyota";

// You can add an element:
cars.push("Audi");
```

But you can NOT reassign the array.

### Constant Objects
```JavaScript
// You can create a const object:
const car = {
	type: "Fiat",
	model: "500",
	color: "white"
};

// You can change a property:
car.color = "red";

// You can add a property:
car.owner = "Johnson";
```

### Browser Support
The `const` keyword is not supported in Internet Explorer 10 or earlier.

### Block Scope
Declaring a variable with `const` is similar to `let` when it cones to **Block Scope**.

#### Example
```JavaScript
const x = 10;
// Here x is 10

{
	const x = 2;
	// Here x is 2
}

// Here x is 10
```

### Redeclaring
Redeclaring an existing `var` or `let` variable to `const`, in the same scope, is not allowed.

Redeclaring an existing `const` variable, in the same scope, is not allowed.

Redeclaring variable with `const`, in another scope, or in another block, is allowed.

### Const Hoisting
Variables defined with const are also hoisted to the top, but not initialized.

Meaning: Using a const variable before it is declared will result in a ReferenceError.

## JavaScript Operators
<++>
