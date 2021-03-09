## array.slice()

a **method** that returns a **shallow copy** of a portion of an array into a new array object selected from start to end where the start and end represent the index of items in that array.

_the original array will **not** be modified_

.slice(start, end)

If end is omitted, slice extracts through the end of the sequence (arr.length).

```
const animalNames = ['ben', 'luna', 'daisy', 'muffin']
let theLadies = animalNames.slice(2,3)

console.log(theLadies) ==> ['luna', 'daisy']
```
