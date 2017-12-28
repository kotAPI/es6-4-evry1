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
