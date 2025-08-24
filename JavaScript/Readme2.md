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

