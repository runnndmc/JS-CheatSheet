## array.slice()

a **method** that returns a **shallow COPY** of a portion of an array into a new array object selected from start to end where the start and end represent the index of items in that array.

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

You can remove elements from teh array by including a deleteCount that will remove the amount indicated from the start of the array. If the deleteCount is negatove or 0, no elements are removed.

You can also add elements to an array by including the item1, item2, etc. values. 

.splice(_start, remove, add_)

```
let myFish = ['angel', 'clown', 'drum', 'mandarin', 'sturgeon']
let removed = myFish.splice(3, 1)

myFish ==> ["angel", "clown", "drum", "sturgeon"]
removed ==> ["mandarin"]

```



