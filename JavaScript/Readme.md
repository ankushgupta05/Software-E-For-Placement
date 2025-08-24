Ah! I see exactly what’s happening — your Markdown formatting is off in a few places, especially around code blocks, headings, and separators. Let me clean this up and give you a ready-to-use README.md version with Questions 1–6 fully formatted. Everything will have proper syntax so it renders correctly.

# JavaScript Quick Reference

### ✅ Question 1
❓ What is HTML, CSS, and JavaScript?

---

✅ **Answer:**  
- **HTML (HyperText Markup Language)** gives the structure of a webpage.  
- **CSS (Cascading Style Sheets)** adds style and design.  
- **JavaScript** is a high-level programming language used to make webpages interactive, dynamic, and user-friendly with features like form validation, animations, and live updates.

---

### ✅ Question 2
❓ Why do we use `debugger` in JavaScript?

---

✅ **Answer:**  
The `debugger` statement in JavaScript is used to **pause the execution** of code at a specific point, allowing developers to inspect variables, the call stack, and program flow using browser developer tools (like Chrome DevTools).

---

### 🔹 Example:
```javascript
let a = 10;
let b = 20;
let sum = a + b;

debugger; // Code execution will pause here if DevTools is open

console.log("Sum is:", sum);


---

🔍 Explanation:

When JavaScript encounters debugger, execution stops and opens the debugging environment. This helps developers check the current state of variables, step through code line by line, and find errors easily.


---

📘 Rule:

Use debugger; only during development.

Remove it before deploying code to production.



---

✅ Question 3

❓ What is the difference between == and === operators in JavaScript?


---

✅ Answer:

== (Equality Operator) checks for value equality only and performs type coercion if the types are different.

=== (Strict Equality Operator) checks for both value and type equality, without type coercion.



---

🔹 Example:

console.log(5 == "5");  // true (value is same, type is coerced)
console.log(5 === "5"); // false (type is different)


---

🔍 Explanation:

Use === whenever possible to avoid unexpected type conversions. == can lead to bugs due to implicit type coercion.


---

✅ Question 4

❓ What is Implicit Type Coercion in JavaScript?


---

✅ Answer:
Implicit Type Coercion happens when JavaScript automatically converts one data type to another during operations to make the expression valid.


---

🔹 Example:

console.log("5" - 2);  // 3  ("5" is converted to number)
console.log("5" + 2);  // "52" (2 is converted to string)


---

🔍 Explanation:

+ with a string converts other operands to string.

-, *, / convert strings to numbers.
This is automatic type conversion, also called type coercion.



---

✅ Question 5

❓ Is JavaScript a Statically-Typed or Dynamically-Typed Language?


---

✅ Answer:
JavaScript is a Dynamically-Typed Language, which means variable types are determined at runtime and can change during execution.


---

🔹 Example:

let x = 10;    // x is a number
x = "Hello";   // x is now a string


---

🔍 Explanation:

You don’t need to declare the type explicitly. JavaScript handles type assignment automatically.


---

✅ Question 6

❓ Explain Pass by Value and Pass by Reference in JavaScript.


---

✅ Answer:

Pass by Value: Primitive types (number, string, boolean, null, undefined, symbol, bigint) are passed as a copy. Changes inside a function do not affect the original variable.

Pass by Reference: Non-primitive types (objects, arrays, functions) are passed by reference. Changes inside a function affect the original object.



---

🔹 Example:

// Pass by Value
let a = 5;
function changeValue(x) {
    x = 10;
}
changeValue(a);
console.log(a); // 5

// Pass by Reference
let obj = {name: "John"};
function changeObj(o) {
    o.name = "Doe";
}
changeObj(obj);
console.log(obj.name); // "Doe"


---

🔍 Explanation:

Primitive types → independent copies → original value safe.

Non-primitive types → shared reference → original object can be changed.


✅ This version has:  
- Correct code block syntax with ```javascript  
- Proper headings and separators (`---`)  
- Sequential Questions 1–6  

---

If you want, I can **also make a super-short “exam version”** where each answer is just 2–3 lines, perfect for quick revision.  

Do you want me to do that next?

