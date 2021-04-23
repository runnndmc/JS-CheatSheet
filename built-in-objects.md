 **all of JavaScript's standard, built-in objects, including their methods and properties. These are objects in the global scope**
 
 ## Math.max()
 
 a function that returns the largest of the zero or more numbers given as input parameters.
 If any parameter isnt a number or can't be converted into one NaN is returned.
 
 ```
 console.log(Math.max(1,2,3) ==> 3
 console.log(Math.max(-1,-2,-3) ==> -1
 
 const arr = [3,2,1,4,5]
 console.log(Math.max(...arr) ==> 5
 
 ```
 
 > Math.max([value1[, value2[, ...]]])
 > 

value1, value2, ... - Zero or more numbers among which the largest value will be selected and reeturned

*Return Value*
The largest of the given numbers. 














 ## toString()
 
 a method that returns a string representing the object.
 
 ```
function Dog(name){
  this.name = name;
 }
 
 const dog1 = new Dog("daisy")
 
 Dog.prototype.toString = function dogToString() {
  return `${this.name}`
 }
 
 console.log(dog1.toString())
 ==> "Daisy"
 
 - or - 

const num = 789
const numStr = num.toString()

console.log(numStr) ==> "789"
 
 ```
 
 > object.toString()
 

*Parameters* (optional)
For numbers and BigInts toString() takes an optional parameter *radix* the value of the radix must be minimum 2 and maximum 36

By using the radix parameter you can also convert base 10 numbers (like: 1,2,3,4,5..) to another base numbers. 

In the example below, there is a converting from base 10 number to a base 2 (binary) number.

ex:
```
let baseTenInt = 10
console.log(baseTenInt.toString(2))
==> "1010"

- same for big integers - 

let bigNum = BigInt(20)
console.log(bigNum.toString(2))
==> "10100"
```

*Return Value*
A string with the object value.
