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

**OR**

if you want to replace all of one value in a string, you can use a regular expression saved to a variable to then include the global and ignore case flags. This permits replace() to replace **each occurrence** 

ex:
```
let re = /apples/gi
let str = "these apples are not apples at all, they're plums!"

let newStr = str.replace(re, 'peaches')
console.log(newStr) => "these peaches are not peaches at all, they're plums!"

```

## string.substring()

a **menthod** that returns the part of the string between the beginning and ending index given.

If there is just the beginning index listed then it will go to the end of the string.

**string.substring(indexStart[,indexEnd])**

If the indexStart is greater than the indexEnd it would act as if the two arguments were swapped. Any argument value that is NaN is treated as a 0.

ex:
```
let str = 'hello world'
let cut = str.substring(1,4)

console.log(cut) ==> 'ello'

let cutOne = str.substring(1, 0)
console.log(cutOne) ==> 'h'
```

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
