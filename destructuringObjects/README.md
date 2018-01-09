# Destructuring Objects

It's pretty important task for a programmer to deal with a lot of data on a daily basis when building web applications.
Lots of APIs respond with JSON objects that need to be **destructured** before you can operate on it, previously, you'd have
to declare a lot of variables spread across a lot of lines making the variable space congested. 

ES brings better features for us to destructure objects in an elegant fashion.

### Destructuring objects into variables

```javascript
var object = {
  first_name: "John",
  last_name : "Wick"
}

const {first_name,last_name} = object
console.log(first_name)
console.log(last_name)
// => John
// => Wick
```

### Customizing variable names
Using the same variable name as in the objects might not be a desired way always, you can give them another variable name by declaring them this way.

```javascript
var object = {
  first_name: "John",
  last_name : "Wick"
}

const {first_name: myFirstName,last_name:myLastName} = object
console.log(myFirstName)
console.log(myLastName)
// => John
// => Wick
```

### Declaring default variables
Let's say your object doesn't have a variable __age__, you can assign variables some said initial values in case they are undefined.
```javascript
var object = {
  first_name: "John",
  last_name : "Wick"
}

const {first_name="John",last_name="Doe",age=27} = object
```
