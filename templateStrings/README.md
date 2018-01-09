# Template Strings

If you ever had been in a situation where you wanted to type in multiline strings and had to use `/` to escape newlines, this
looked bad and felt out of place to write code this way.  

```javascript
var a= "asdasdaadsad \
asdasdadsasd\
asdasdasdasdada\
"
```

ES6 now includes _template strings_ or _template literal strings_. You can forget about using the `/` to escape newlines, just
type in your text between the backticks `

```javascript
var a =`
asdasdasd
asdasdasd
asdasdads
    asdads  asdasdas dsaasdd aasd
asdasd asdasdas asdasd
`
```

This makes injecting HTML into the DOM with JavaScript a lot easier than it was.
```javascript
var person = {
    name : "Keanu Reeves",
    type: "Actor",
    age : "Immortal",
    bio : "The One"
}

var markup = `
    <div>
        <ul>
            <li>${person.name}</li>
            <li>${person.type}</li>
            <li>${person.age}</li>
            <li>${person.bio}</li>
        </ul>
    </div>
`
document.querySelector("body").innerHTML = markup
```

It is a great improvement over appending string with markup across many lines. Note that, you'd also be storing the indent spaces as a part of the string too!

