## What is JS?
A programming language that conforms to the ECMAScript standard as a way to add programs to web pages. It's a dynamic language that creates modern web applications where you can interact directly **without doing a page reload for each action**. JavaScript is prototype-based, multi-paradigm language that is object oriented and functional programing styles.

## Main Data Types in JS:
+ Numbers
+ Strings
+ Boolean 
+ Null 
+ Undefined
+ Symbol 
+ Object


## What are Special Numbers in JavaScript?
Special numbers are: Infinity, -Infinity, NaN (even though it is a value of the number type)


## How does a program keep an internal state?
JavaScript provides a binding or a variable to set internal state

```
let ten = 10
console.log(ten * ten)
==> 100
```

the keyword let indicates that this sentence is going to define a binding called ten. 
After the binding has been defined its name can be used as an expression. 
The value od such an expression is the value that the binding currenty holds. 

## What is a JavaScript Environment?
A JS environment is a collection of bindings and their values that are defined and exist at a given time.

## What is a function?
a function is a piece of program wrapped in a value that can be applied in order to run the wrapped program. 
Special values that wrap a piece of a program. 

## What is a conditional execution?
A conditional execution is where the program takes the proper branch based on the situation indicated. - created with an if statement 

## How would you introduce disturbances in the control flow?
By introducing a conditional statement (if, else, switch) or with looping statements (while, do, for)

## What creates a function value? 
When you use the function keyword as an expression. 

# What is the difference between a function expression and a function declaration?
The main difference between a function expression and a function declaration is the function name,
The function name can be omitted in function expressions to create *anonymous functions.*
A function expression can be used as an IIFE (Immediately Invoked Function Expression) which runs as soon as it is defined.

# Are function expressions hoisted in JS?
No, function expressions can not be hoisted in JS. 
This is because you cant use function expressions before you create them.
With function declarations you can use a function before it is declared.

```
//function declaration: 

hoisted(); ==> logs "moo"

function hoisted() {
  console.log('moo');
}

========================

function expression: 

notHoisted(); ==> TypeError: notHoisted is not a function

var notHoisted = function() {
   console.log('bar');
};

```
## What happens when you use function as a statement?
It can be used to declare a binding and give it a function as its value. 

## What is scope?
Part of the program in which the binding is visible. The scope could either be local, global or lexical (nested).

## How are properties accessed in JS?
value.prop ----- or ------ value["prop"]

## What are methods?
functions that live inside properties and usually act on the value they are a property of. 

## What is an abstraction?
Abstractions hid the details and give us the ability to talk about problems at a higher or more abstract level. 

## What are higher order functions?
Higher order functions are functions that operate on other functions either by taking them as arguments or returning them. This allows us to abstract over actions and not just values. 

## What is the difference between forEach and .map? 
forEach loops through the elements in an array and does not return any values once it has been run. On the other hand .map performs a function on each value of an array and returns a transformed array with new values performed by the function.

## What is a regular expression?
objects that represent patterns in strings. They use their own language to express these patterns.

## What string methods are used for regular expressions?
 .match() / .replace() / .search()

## What is Asynchronous programming?
Async programming makes it possible to express waiting for long running actions without freezing the program during these actions. This style of programming can be implemented using callbacks and an event loop schedules such callbacks to be called when the actions complete. 

## What is a promise? 
A Promise consists of objects that represent actions that might complete in the future. Async functions allow you to write an async program as if it were synchronous.

## What is the DOM?
A data structore that represents the browsers model of the document and a JavaScript program can modify it to change the visible document.


## How does the Http protocol work?
A client sends a request that contains a method and a path that identifies a resource. The server then decides what to do with the request and responds with a status code and a response body. 

## What is a fetch request?
The interface through which browser JavaScript can make HTTP requests.

## What is the difference between local and session storage?
Local storage saves information forever or until the user decides to clear it. Session storage saves the information until the browser is closed. 

You can store items in local storage by using setItem(), getItem(), removeItem(), clear() or key()

Local storange can only store strings. 
To store objects or arrays you can first use JSON.stringify() method before passing .setItem()

```
const person = {
  name: "Dayna",
  gender: "female"
 }

window.localStorage.setItem('user', JSON.stringify(person))
```
