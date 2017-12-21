# es6-4-evry1
thiz iz es6 4 evry1

# _var_, _let_ and _const_
**_var_** is function scoped

When a variable is declared in a function, a new memory chunk is allocated to that variable. If it's declared with a `var` keyword inside the function, it lives inside that function. It cannot be accessed outside the function.
```javascript
function scopeFunc(){
  var a = 2;
}
console.log(a)
// => a is not defined <Uncaught referenceError> 
```

But, this doesn't apply to **block**s. The scope leaks outside the `if` block and the `console.log` picks up the variable and prints it's value.

```javascript
if(true){
  var a=2;
}
console.log(a)
// => 2
```
Be careful when using **var** inside blocks, if possible try avoiding them at all costs. Restrict the usage to var to functions only. Use **_let_** or **_const_** instead.

**_let_** 

Just like **var**, **let** is used to declare variables, unlike **var** it's block scoped.
```javascript
if(true){
  let a=2;
}
console.log(a)
// Uncaught ReferenceError: a is not defined
```

Another point to note about **let** is that, you cannot redefine a variable like you can do with **var**
With **var**, this is totally accepted.

```javascript
var a = 2;
var a = 22;
```
But with **let**, you cannot redefine a variable like **var**
```javascript
let a = 2;
let a = 22;
// => Uncaught SyntaxError: Identifier 'a' has already been declared
```

## **let** lives as a unique variable in every separate block
The **let** you declare in every block is unique to it's own block, take proper care when using them in blocks.

```javascript
let a = 2;
if(true){
  let a = 22;
}
console.log(a)
// => 2
```
Pay attention to the above example, the variables a=2 and a=22 are separate variables, they might have the same name, but they're separate variables.

__Best Practice__ : Avoid using same variable names throughout the program even if it's block scoped.

## **const**
**const** is similar to let, it lives in a block scope, the main difference between **let** and **const**, you can change the value of **let**, but with **const**- you cannot change its value once declated. 

```javascript
 if(true){
  const a = 22
}
console.log(a)
```


Also note that **const** needs to be defined with a value.

```javascript
const a;
//==> Uncaught SyntaxError: Missing initializer in const declaration
```
On the other hand, JavaScript __const__ objects are mutable. 

```javascript
const myObj = {
  val:2,
  index:1
}
myObj.val = 2
console.log(myObj.val)
// => 2
```
The object attributes can be changed, but the object itself cannot be reassigned to something else.

```javascript
const myObj = {
  val:2,
  index:1
}
var someOtherObj = {
  garbage:"garbage-value",
  someOtherGarbage:"Some Other Garbage Value"
}

myObj = someOtherObj
// => Uncaught TypeError: Assignment to constant variable.
```


