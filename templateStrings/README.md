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
