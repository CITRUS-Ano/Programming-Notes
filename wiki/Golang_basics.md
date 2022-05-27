# Golang basics
### Create a project in Golang
#### Check the workplace
```command line
go env GOPATH
```

#### Create source code directory
```command line
cd go
mkdir src
```

#### Open go module features and initialize go module
```command line
go env -w GO111MODULE=on
go mod init directory_name
```

#### Go to project directory and create .go file
```command line
cd learn-go
nvim main.go
```
---

### Package and main function
#### Declares which package in the project the file is
```Golang
package main
```

*It's necessary to need a main package to run a project* 

#### Main function
```Golang
func main() {
  
}
```
*Main function has no parameters and no return values* 

#### Import other packages
```Golang
import (
  "package_name"
  "fmt"
)
```
---

### Run a project
#### Run golang file
1. Run golang file directly
```command line
go run main.go
```

2. Build to executable file and then run it
```command line
go build
./learn-go
```

3. Build to executable file in workspace bin
```command line
go install
../../bin/learn-go
```

---
### Basic syntax
#### Define a variable
1. var + variable_name + data_structure
```Golang
var a int // error: if a declared but not used
```
*If variable is not defined a value, it will have initial value. like int as 0 and string as ""*

2. variable_name := value
```Golang
a := 3  // Golang will determine the data structure by value
```

#### Logical judgement
1. if ... else if ... else
```Golang
if (_expression) {
  _statement1
} else if {
  _statement2
} else {
  _statement3 
}
```

2. && and ||
```Golang
if (_expression1 &&(||) _expression2) {
  _statement
}
```

#### Loop through
1. Basic for lopp
```Golang
// like C language
for i := 0; i < 5; i++ {  // Golang don;t support ++i
  _statement
}
```

*Ignore executed one time and every time statements is similar like while loop*
```Golang
for ; i < 5; { // semicolons can all ignored
  _statement
}
```

*Every statements in for loop can be ignored and don't need use semicolons*

2. literate over the array
```Golang
for k, v := range arr { // k: index, v: value
  _statements
}
```

3. literate over the dictionary
```Golang
for k, v := range dic { // k: key, v: value
  _statements
}
```

---


### Basic the type of data
#### Tuple or array
1. Define a tuple or array
```Golang
var x [3]int
var y := [3]int{1, 2, 3}
```

2. Modify the value of the corresponding index
```Golang
x[1] = 9
```
*Index start from 0*

3. Define a slice
```Golang
x := []int{1, 2, 3} // no longer define the size of tuple
x = append(x, 10) // the size of the tuple will be doubled then copy elements to new tuple and release old tuple
```

#### Dictionary
1. Create a dictionary
```Golang
// the data structure of key is in square brackets and the data structure of value is followed by it
numbers := make(map[String]int)
```

2. Append or remove a elements in dictionary
```Golang
// add elements
numbers["one"] = 1
numbers["two"] = 2

// delete elements
delete(numbers, "one")
```

---


### Function
#### Define a function
1. Return one or multiple values
```Golang
// Golang can return multiple values
func func_name(_param1 _dtype, ...) (return1_type, ...) {
  // code block to be executed
  return return_value1, ...
}
```

2. Closure: return a function
```Golang
func func_name(_param1 _dtype, ...) (return1_type, ...) {
  // code block to be executed
  return func ()
}
```


---

### Pointer
#### Simple use of pointers
```Golang
func increase(n *int) {
  *n = *n + 1
  
func main() {
  n := 0
  increase(&n)
}
```

---


### Declare custom data types
#### Define a data type by a basic data type
```Golang
type MyFloat float65
```

#### Define a data type by struct
```Golang
type cat struct {
  name string
  age int
}
```

*define out of main function* 

#### use custom data types
1. call a custom data type
```Golang
func main() {
  newCat := cat{name: "kitty", age: 3}
}
```

2. Modify values in struct
```Golang
newCat.age = 4
```

#### Define a function for custom types
```Golang
type MyFloat float64

func (n MyFloat) show() { // variable only MyFloat type can call this function
  _statement
}
```

#### a function in custom type also can use pointer to save values
```Golang
func (n *MyFloat) add() {
  *n = *n + 0.5
}
```


