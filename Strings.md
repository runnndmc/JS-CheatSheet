## string.replace() 

a **method** that returns a **new** string with some or all matched of a pattern replaced by a replacement.

ex: 
```
let str = 'hello there'

let newStr = str.replace('there', 'friend');
console.log(newStr) ==> 'hello friend'
```

if there are multiple values that are the same - 
ex. "hello there there" - it would only replace the first one and not the second

you could instead use .replaceAll() 

## string.split()

a **menthod** that takes a string and divides it into an ordered list of sub strings that are put into an **array** and returns the array.

The method divides (or splits) the string where the pattern is located.

**string.split([seperator[,limit]])**

a limit is optional but is a non-negative integer that specifies the limit on the number of substrings to be included in the array

ex:
```
let str = 'hello world'
let cut = str.split(' ')

console.log(cut) ==> ['hello', 'world']

let cutOne = str.split(' ', 1)
console.log(cutOne) ==> ['hello']
```
