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
