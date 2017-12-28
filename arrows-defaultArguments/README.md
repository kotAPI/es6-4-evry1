# Arrow Functions

ES6 introduces a new way to write arrow functions, this provides a few notable advantages over the old style.
You'd write a basic arrow function like this..
`Todo - browser support`

```javascript
const greetMe = (name)=>{
    return "Hello! "+name
}

greetMe("John Oliver!") // => "Hello! John Oliver!"
```
Arrow functions make your functions look more elegant, they reduce a significant amount of keystrokes to write a function.
The above example is a short hand way to write functions in ES6, also an *explict* way to return. You could make it even shorter this way and an *implicit* return..

```javascript
const greetMe = (name)=>"Hello! "+name

greetMe("John Oliver!") // => "Hello! John Oliver!"
```

What if my function doesn't take arguments?
Easy, just give an empty parenthesis `()`


```javascript
const greetMe = ()=>"Hello!"

greetMe() // => "Hello!"
```
That sounds about right, wait.. no brackets when I return? How do I return an Object in that case?
The trick is to add parenthesis `()` around your object.

```javascript
const objectReturner = (name,age,place) =>({name:name, age:age, place:place})
objectReturner("Elton John","56","New York") 
//=> {name: "Elton John", age: "56", place: "New York"}
```

## Scoping behaviours with arrow function

ES6 arrow functions are great, but they aren't meant to be used everywhere. The reference of `this` changes when you use the arrow functions. 

Better demonstrated with an example 
```javascript
this.foo = {a:20}

var obj = {
	foo:{a:2},
	getter:function(){
		console.log(this.foo)
	}
}

obj.getter() //=> {a:2}
```

Now, rewriting the above example in ES6.

```javascript
this.foo = {a:20}

var obj = {
	foo:{a:2},
	getter:()=>{
		console.log(this.foo)
	}
}

obj.getter() //=> {a:20}
```
`this` here takes the scope of the parent relative to the function's scope. This is both advantage and a disadvantage when using arrow functions, so proper care needs to be taken when writing code with arrow functions.
