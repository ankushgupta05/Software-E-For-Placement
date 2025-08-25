Perfect 👍 I’ll keep 13 as it is and just add 14, 15, 16 in the same list.


---

13. What Are the Different Types of Errors in JavaScript?
In JavaScript, errors occur when the program breaks due to invalid code or unexpected behavior. The main types are:

Syntax Error – Occurs when code is written incorrectly (e.g., missing brackets, semicolon).

Reference Error – When trying to use a variable that is not defined.

Type Error – Happens when a value is not of the expected type (e.g., calling a number as a function).

Range Error – When a value is not within the allowed range (e.g., new Array(-5)).

Eval Error – Related to the eval() function (rarely used in modern JavaScript).

URI Error – When incorrect decodeURI() or encodeURI() functions are used.



---

14. What Is Memoization in JavaScript?

Memoization means saving function results so that next time the same input comes, it does not calculate again.

It makes the program faster.


👉 Example:

function add(a, b) {
  console.log("Calculating...");
  return a + b;
}

let cache = {};
function memoAdd(a, b) {
  let key = a + "," + b;
  if (cache[key]) {
    return cache[key];   // return saved value
  }
  cache[key] = add(a, b); // save result
  return cache[key];
}

console.log(memoAdd(2, 3)); // Calculates
console.log(memoAdd(2, 3)); // Uses saved value


---

15. What Is the Use of a Constructor Function in JavaScript?

Constructor function is used to make many objects quickly.

It works like a blueprint.

Always used with new keyword.


👉 Example:

function Car(name, model) {
  this.name = name;
  this.model = model;
}

let c1 = new Car("Toyota", 2022);
let c2 = new Car("Honda", 2023);

console.log(c1.name); // Toyota


---

16. What Is the Difference Between == and === in JavaScript?

== → checks only value (does type conversion).

=== → checks value and type both (strict checking).


👉 Example:

console.log(5 == "5");  // true  (only value checked)
console.log(5 === "5"); // false (type different: number vs string)


---

Do you want me to also extend this list with 17, 18, 19 in the same easy and short style?






Got it 👍 I’ll write your given questions as 20, 21, 22 in the same easy style we used earlier.


---

20. What Is the Difference Between null and undefined?

null → an empty value (set by the programmer). It means "nothing".

undefined → means a variable has been declared but not given any value.


👉 Example:

let a;
console.log(a);     // undefined (no value given)

let b = null;
console.log(b);     // null (empty value)


---

21. What Is Event Delegation in JavaScript and Why Is It Useful?

Event Delegation means attaching a single event listener to a parent element instead of adding listeners to each child element.

It is useful because:

1. Saves memory (less event listeners).


2. Works even for dynamically added elements.




👉 Example:

document.getElementById("list").addEventListener("click", function(e) {
  if (e.target.tagName === "LI") {
    console.log("You clicked: " + e.target.innerText);
  }
});

Here, instead of giving click event to each <li>, we gave it once to <ul>.


---

22. Explain the Concept of Prototypes in JavaScript.

Every object in JavaScript has a prototype.

Prototype is like a hidden object from which other objects inherit properties and methods.

It helps in reusing methods without copying them.


👉 Example:

function Person(name) {
  this.name = name;
}

// add method to prototype
Person.prototype.sayHello = function() {
  console.log("Hello, I am " + this.name);
};

let p1 = new Person("Alice");
p1.sayHello(); // Hello, I am Alice

Here, sayHello() is not inside the object directly, it comes from the prototype.


---

👉 Do you want me to continue with 23, 24, 25 (your 25 is missing) and 27 in the same simple style?




Got it 👍 I’ll keep them very simple but add a little more explanation so you can explain clearly in interviews.


---

23. How Can You Clone an Object in JavaScript?

Cloning means making a copy of an object.

If we change the copy, the original should not change.

Ways:

Shallow copy (copies only top level):

let obj = {a: 1, b: 2};
let clone1 = {...obj};               
let clone2 = Object.assign({}, obj);

Deep copy (copies nested objects also):

let deep = JSON.parse(JSON.stringify(obj));




---

24. What Are Arrow Functions in JavaScript?

Arrow functions are a short form of functions.

They make code smaller and easier to read.

They do not have their own this, they use the parent this.


👉 Example:

let add = (a, b) => a + b;
console.log(add(2,3)); // 5


---

25. Difference Between let, const, and var

var → Old way, function-scoped, can re-declare and change.

let → New way, block-scoped, can change value but not re-declare in same block.

const → Block-scoped, value cannot change (constant).


👉 Example:

var x = 10;  // old, function scope
let y = 20;  // block scope, can update
const z = 30; // block scope, cannot update


---

26. What Are Promises in JavaScript?

Promise is used to handle asynchronous work (something that takes time like API calls).

It has 3 states:

1. pending → work not finished yet.


2. resolved → work finished successfully.


3. rejected → work failed.




👉 Example:

let promise = new Promise((resolve, reject) => {
  resolve("Success!");
});

promise.then(res => console.log(res)); // Success!


---

27. What Is a Generator Function?

A special function that can pause with yield and resume later.

Declared with function*.

Useful for working step by step.


👉 Example:

function* numbers() {
  yield 1;
  yield 2;
  yield 3;
}
let gen = numbers();
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2


---

28. WeakMap and WeakSet in JavaScript

WeakMap → Like Map, but keys must be objects. Values are garbage collected if object is not used anywhere else.

WeakSet → Like Set, but it only stores objects (not strings or numbers).


👉 Example:

let wm = new WeakMap();
let obj = {};
wm.set(obj, "data");
console.log(wm.get(obj)); // data

let ws = new WeakSet();
ws.add(obj);
console.log(ws.has(obj)); // true


---



Perfect 👍 I’ll give you complete but very simple definitions for both questions (34 & 35).


---

34. Purpose of async and await in JavaScript

async keyword:

Used before a function.

It makes the function always return a Promise.


await keyword:

Used inside an async function.

It tells JavaScript to wait until the Promise finishes before going to the next line.



✅ Example:

async function example() {
  let promise = new Promise((resolve) => {
    setTimeout(() => resolve("Done!"), 2000);
  });

  let result = await promise; // waits 2 seconds
  console.log(result); // Done!
}
example();

👉 Simple meaning: async/await is used to write asynchronous code in a way that looks simple, like normal step-by-step code.


---

35. Difference Between Function Declaration and Function Expression

Function Declaration

A function created with the function keyword and a name.

It is hoisted, meaning you can call it before it is written in the code.


✅ Example:

greet(); // works

function greet() {
  console.log("Hello from Declaration!");
}


---

Function Expression

A function assigned to a variable (can be anonymous or named).

It is not hoisted, so you can only call it after it is defined.


✅ Example:

// greet(); ❌ Error: Cannot access before initialization

const greet = function() {
  console.log("Hello from Expression!");
};
greet(); // works


---

👉 Simple meaning:

Declaration = defined with a name, can be used before it appears in code.

Expression = stored in a variable, can only be used after it is defined.



---



---

1. Synchronous

Tasks run one after another (step by step).

The next task starts only after the previous one is finished.

It is blocking (you must wait).


👉 Example:
At an ATM machine:

Insert card

Enter PIN

Withdraw money
Each step happens in order, one by one.



---

2. Asynchronous

Tasks can run independently or in the background.

You don’t need to wait for one task to finish before starting another.

It is non-blocking.


👉 Example:
While shopping online:

You place an order (this happens in the background).

At the same time, you can continue browsing other products.

You don’t have to wait for the first order to complete.



---



