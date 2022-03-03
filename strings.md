## string.replace() 

a **method** that returns a **new** string with some or all matched of a pattern replaced by a replacement.

ex: 
```
let str = 'hello there'

let newStr = str.replace('there', 'friend');
console.log(newStr) ==> 'hello friend'
```

if there are multiple values that are the same - 
ex. "hello there there" - it would only replace the *first* one and not the second

you could instead use .replaceAll() 

**OR**

if you want to replace all of one value in a string, you can use a regular expression saved to a variable to then include the global and ignore case flags. This permits replace() to replace **each occurrence** 

ex:
```
const regEx = /apples/gi
const str = "these apples are not apples at all, they're plums!"

const newStr = str.replace(regEx, 'peaches')
console.log(newStr) => "these peaches are not peaches at all, they're plums!"

```

<br></br>


## string.substring()

a **method** that returns the *part* of the string between the beginning and ending index given.

>string.substring(indexStart[,indexEnd])

ex:
```
let str = 'hello world'
let cut = str.substring(1,4)

console.log(cut) ==> 'ello'

let cutOne = str.substring(1, 0)
console.log(cutOne) ==> 'h'
```

If there is just the beginning index listed then it will go to the end of the string.

If the indexStart is greater than the indexEnd it would act as if the two arguments were swapped. 

Any argument value that is NaN is treated as a 0.


<br></br>


## string.split() ['SP','LIT']

a **method** that divides a string into an ordered list of substrings and puts the substrings into an **array**. The division is done by searching for a pattern that is described as the first parameter of the methods call.


>str.split([separator[, limit]])

separator - (optional) the pattern describing where each split should occur. 

If the separator is omitted, the returned arr contains one element consisting of the entire string

limit - (optional) A non-negative integer that specifies a limit on the number of substrings to be included in the array


ex: 
```
let str = 'The Kind Person is Kind'

let strCopy = str.split(' ');
console.log(strCopy) ==> ['The', 'Kind', 'Person', 'is', 'Kind']
```


If included, it splits the string at the pattern but stops when the limit entries have been placed in the array and any leftover text is not included in the array at all. 



<br></br>


## string.chatAt() 

a **method** that returns a *new string* consisting of the single UTF-16 code unit located at the specified offset into the string.

ex: 
```
const str = 'The quick brown fox'

const index = 4

console.log(str.charAt(index)) 
===> 'q'

console.log(`The character at index ${index} is ${str.charAt(index)}`)
  ==> 'The character at index 4 is q'
```

**let characher = str.charAt(index)**

index - an integer between 0 and str.length -1. If the index cannot be converted to the integer or no index is provided, the default is 0 so the first character of str is returned 


<br></br>


## string.repeat() 

a **method** that returns a new string that contains the specified number of copies od the string on which it was called all concatenated together.


ex: 
```
let str = 'Today is a new day.'

console.log(str.repeat(3))
  ==> 'Today is a new day.Today is a new day.Today is a new day.'
  
  
'abc'.repeat(2) ==> 'abcabc'
  
```
> str.repeat(count)

count - an integer between 0 and infinity indicating the number of times to repeat the string.


<br></br>

## string.padStart() 

a **method** that pads the current string with another string (multiple times, if needed) until the resulting string reaches the given length. The padding is applied from the *start* of the current string. 

ex:  
```
const str = '8'

console.log(str.padStart(3,'0'))
  ==> '0008'
  
  
const fullNum = "01234324567565476"
const lastFour = fullNum.slice(-4)
const hiddenNum = lastFour.padStart(fullNum.length, '*')

console.log(hiddenNum) ==> "*************5476"
  
```
> str.padStart(targetLength [, padString))

targetLength - The length of the resulting string once the current str has been padded. If the value is less than str.length then str is returned as is. 

padString - (optional)the string to pad the current str with. If padString is too long, to stay within the targetLength it will be truncated from the end.

<br></br>


## string.match() 

a **method** that retrieves the result of matching a string against a *regular expression*

ex:  
```
const str = 'Am I missing anything?'

console.log(str.match(/[A-Z/g))
  ==> ["A", "I"]
  
 -or-
 
 const str = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz'
 const regexp = /[A-E]/gi;
 const matchesArr = str.match(regexp)
 
 console.log(matchesArr) ==> ["A", "B", "C", "D", "E", "a", "b", "c", "d", "e"]
  
```

> str.match(regexp)

regexp - if regexp is a non-regexp object, it is implicitly converted to a regexp by using new RegExp(regexp)

if you dont have a parameter, you will get an Array with an empty string: [""]

<br></br>

## str.trim()

removes white spaces from both ends of a string and returns a new string without modifying the original string.


```
ex:

const str = "     hello     "
console.log(str.trim()) ==> "hello"

```


<br></br>
