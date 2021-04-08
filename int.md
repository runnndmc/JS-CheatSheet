### Integers 

## Int to Array 

Converting integers into an array:
```
const numbers = 159361
const arr = Array.from(String(numbers), Number)

console.log(arr) ==> [ 1, 5, 9, 3, 6, 1 ]
```

> Array.from()
creates a **new** shallow-copies Array instance from an iterable object 

```
console.log(Array.from('day')) => Array ["d", "a", "y"] 
```

> String(numbers)
creates a string by performing a type conversion
```
const numbers = 159361
const arr = String(numbers)

console.log(arr) ==> "159361"
```

> Number
The Number constructor contains constants and methods for working with nummbers
