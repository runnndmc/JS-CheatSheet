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

## string.split() 

a **method** that divides a string into an ordered list of substrings and puts the substrings into an **array**. The division is done by searching for a pattern that is described as the first parameter of the methods call.

ex: 
```
let str = 'The Kind Person is Kind'

let strCopy = str.split(' ');
console.log(strCopy) ==> ['The', 'Kind', 'Person', 'is', 'Kind']
```

**str.split([separator[, limit]])**

separator - (optional) the pattern describing where each split should occur. 

If the separator is omitted, the returned arr contains one element consisting of the entire string

limit - (optional) A non-negative integer that specifies a limit on the number of substrings to be included in the array

If included, it splits the string at the pattern but stops when the limit entries have been placed in the array and any leftover text is not included in the array at all. 
