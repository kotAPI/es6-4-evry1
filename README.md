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
Be careful when using variables inside blocks, if possible try avoiding them at all costs. Restrict the usage to var to functions only. Use **_let_** or **_const_** instead.

**_let_** 
