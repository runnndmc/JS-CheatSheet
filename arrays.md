## array.slice()

a **method** that returns a **shallow COPY** of a portion of an array into a new array object selected from start to end.
The start and end represent the index of items in that shalllow copy array.

_the original array will **not** be modified_

> arr.slice(start, end)

If end is omitted, slice extracts through the end of the sequence (arr.length).

```
const animalNames = ['ben', 'luna', 'daisy', 'muffin']
let theLadies = animalNames.slice(2,3)

console.log(theLadies) ==> ['luna', 'daisy']
```

## array.splice();

a **method** that **CHANGES an array** by adding or removing elements from it.  

> let newArr = arr.splice(**start**[, deleteCount[, item1[, item2[, ...]]]])

If the start is negative, it will begin that many elements from the _end_ of the array.

You can remove elements from the array by including a deleteCount that will remove the amount indicated from the start of the array. If the deleteCount is negative or 0, no elements are removed.

You can also add elements to an array by including the item1, item2, etc. values. 

.splice(_start, remove, add_)

```
let myFish = ['angel', 'clown', 'drum', 'mandarin', 'sturgeon']
let removed = myFish.splice(3, 1)

myFish ==> ["angel", "clown", "drum", "sturgeon"]
removed ==> ["mandarin"]

```

## array.filter();

a **method** that **creates a NEW array** with all the elements that pass test given by the preceeding function.  

```
let newArr = arr.filter(callback(currentCalue[, index[, array]]) { 
  // return element for new Array, if true
}[, thisArgument]);
```

callback - function to test each element of the array and return true elements
currentValue - current element being processed in the array 

index(optional) - the index of the current element being processed in the array 
array(optional) - an array that the originial filter was called upon 

thisArgument(optional) - a value to use as 'this' when executing callback


```
function isBigEnough(value){
  return value >= 10;
}

let newFilteredArray = [12, 5, 8, 130, 44].filter(isBigEnough)

newFilteredArray ==>[12, 130, 44]
```

## array.includes();

a **method** that determines whether an array includes a certian value in it's entries. This returns a true or false 

```
arr.includes(valueToFind[, fromIndex])

```

valueToFind - what to search for

fromIndex (optional) - the position in the array where to start the search

If fromIndex is greater than or equal to the length of the array, false is returned. The array will not be searched.

```
let arr = [1, 2, 3]

arr.includes(1) => true
arr.includes(7) => false
arr.includes(1, 100) => false
arr.includes(1, 3) => false
```

## array.indexOf();

a **method** that returns the first index at which a given element can be found in the array or -1 if it is not present.

```
arr.indexOf(searchElement[, fromIndex])

```

## array.reduce();

a **method** that executes a reducer your provided function on each element of the array - resulting in a single output value.



```
const arr = [3, 5, 9, 9]
const reducer = (accumulator, currentValue) => accumulator + currentValue

console.log(arr.reduce(reducer)) ==> 26
```

```
let flattened = [[0, 1], [2, 3], [4, 5]].reduce(
  function(accumulator, currentValue) {
    return accumulator.concat(currentValue)
  },
  []
)
// flattened is [0, 1, 2, 3, 4, 5]
```


>arr.reduce(callback (accumulator, currentValue, [, index[, array]] )[, initialValue])



callback - a function to execute on each element in the array *except the first is no initialValue is supplied*

The callback takes the arguments: 

accumulator - the accumulator accumulates the callback's return values. It is the accumulated value previously returned in the last invocation of the callback -- or the initialValue if supplied

currentValue - The current element being processed in the array

index (optional) - The index of the current element being processed in the array. Starts at index 0 if an initialValue is provided. Otherwise it starts from index 1.

array (optional) - The array reduce() is being called upon 

initialValue - a value to use as the first argument to the first call of the callback. Calling reduce() on an empty array without an initialValue will throw a typeError


## array.join();

a **method** that creates and returns a new **String** by concatenating all of the elements in an array (or array-like object) seperated by commas or specified by a seperator sting.


>arr.join([seperator])

seperator(optional) - Specifies a string to seperate each pair of adjacent elements of the array. The seperator is converted to a string if necessary. 

---> If the seperator is omitted, the array elements are separated with a comma. 

```
const arr = ["Wine", "Beer", "Liquor", "Seltzer"]


console.log(arr.join()) ==> "Wine,Beer,Liquor,Seltzer"
console.log(arr.join(', ')) ==> "Wine, Beer, Liquor, Seltzer"
console.log(arr.join(' + ')) ==> "Wine + Beer + Liquor + Seltzer"
console.log(arr.join('')) ==> "WineBeerLiquorSeltzer"

```

## array.unshift();
### adds | beginning | new length

a **method** that **adds** one or more elements to the beginning of an array and returns the **new length** of the array.


>unshift(element0)
>unshift(element0, element1)
>unshift(element0, element1, ... , elementN)

element - The elements to add to the front of the arr. 

---> returns the new length property of the object upon which the method was called. 

```
const arr = [4,5,6]

console.log(arr.unshift(1,2,3)) ==> [1,2,3,4,5,6]

arr.unshift(1)
arr.unshift(2)
arr.unshift(3)

console.log(arr) ==> [3,2,1,4,5,6]

```

## array.shift();

### removes | beginning | removed element

a **method** that removes the first element from the **beginning** of an array and <br>*returns the **removed element**.* This method changes the length of the array.


>shift()


---> returns the removed element from the array or undeifned if the array is empty

```
const arr = [7,8,9]

arr.shift() ==> 7

console.log(arr) ==> [8,9]

```

## array.reverse();

A method that reverses the order of the elements in an array. This method over writes the original array.

```
const array = [7,8,9]

array.reverse()

console.log(array) ==> [9,8,7]
```

## array.every();

A method that tests whether all elements in the array passs the teest implemented by the provided function. Returns a boolean value.
```
const isBelowThreshold = (currentValue) => currentValue < 40

const array = [1, 30, 39, 29, 10, 13];

console.log(array1.every(isBelowThreshold));
==> true
```

