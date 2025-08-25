Alright 👍 Here’s a simple explanation of each in English with numbering (36, 37, 38, 39):


---

36. How Do You Handle Errors in JavaScript?

Errors in JavaScript are handled using the try...catch...finally block.

try → code that may cause an error.

catch → handles the error if it happens.

finally → runs code always (error or not).


👉 Example:

try {
  let num = 10 / 0;
  console.log(num);
} catch (error) {
  console.log("Error occurred: " + error.message);
} finally {
  console.log("This runs always.");
}



---

38. What Is the Difference Between querySelector and getElementById?

getElementById(id)

Finds an element only by its ID.

Returns one element.


querySelector(selector)

Finds the first element that matches a CSS selector (id, class, tag, etc.).

More powerful but may be slower.



👉 Example:

document.getElementById("myId");      // Only by ID
document.querySelector(".myClass");   // By class
document.querySelector("#myId");      // By ID (like getElementById)


---

39. What Is the Purpose of the setTimeout() Function in JavaScript?

setTimeout() is used to delay the execution of a function.

It runs the code once after a given time (in milliseconds).


👉 Example:

setTimeout(function() {
  console.log("Hello after 2 seconds!");
}, 2000);

(Here the message prints after 2 seconds.)


---

Do you want me to also cover setInterval() vs setTimeout() (since they are often asked together)?


Got it 👍 Let’s explain Event Bubbling in easy technical English:


---

🔹 What is Event Bubbling?

When you click (or trigger an event) on a child element, the event does not stop there.

It moves upward to the parent, then grandparent, then all the way up to the document.

This upward flow is called event bubbling.


👉 Flow = Child → Parent → Grandparent → Document


---

🔹 Example

<div id="parent">
  <button id="child">Click Me</button>
</div>

document.getElementById("parent").addEventListener("click", () => {
  console.log("Parent clicked");
});

document.getElementById("child").addEventListener("click", () => {
  console.log("Child clicked");
});

👉 If you click the button:

First → "Child clicked"

Then → "Parent clicked"


Because the event bubbled from child to parent.


---

🔹 How to Stop It?

1. event.stopPropagation()

Stops the event from going to parent.

document.getElementById("child").addEventListener("click", (event) => {
  console.log("Child clicked");
  event.stopPropagation(); // ✅ stops bubbling
});

Now only "Child clicked" will show.


---

🔹 Simple Summary

Event Bubbling = Event moves upward (child → parent).

Problem = Sometimes parent event runs by mistake.

Solution = Use stopPropagation() to stop it.



---

Do you want me to also explain the opposite (Event Capturing: parent → child) in the same simple way?






Got it 👍 I’ll give you the complete definitions in easy English (same style as previous answers).
Let’s continue with 40, 41, 42, 43, 44:


---

40. How Can You Prevent the Default Behavior of an Event in JavaScript?

In JavaScript, some HTML elements have a default action.

Example: Clicking a link <a> opens another page.

Example: Submitting a form <form> reloads the page.


If you don’t want this to happen, you can use event.preventDefault() inside the event handler.

👉 Example:

document.querySelector("a").addEventListener("click", function(event) {
  event.preventDefault(); // stops opening the link
  console.log("Default action prevented!");
});

✅ Definition: preventDefault() is used to stop the browser’s default behavior for an element’s event.


---

41. What Is the Difference Between localStorage and sessionStorage in JavaScript?

Both are part of the Web Storage API and are used to store data in the browser.

localStorage

Stores data with no time limit.

Data stays even after the browser is closed and reopened.

Shared between all tabs/windows of the same site.


sessionStorage

Stores data only for the current session/tab.

Data is removed when the tab or browser is closed.

Not shared across tabs.



👉 Example:

localStorage.setItem("name", "Alice");   // saved permanently
sessionStorage.setItem("age", "22");     // removed when tab closed

✅ Definition: localStorage saves data permanently (until cleared), while sessionStorage saves data only for one tab session.


---

42. How Can You Convert a String to Lowercase in JavaScript?

You can use the toLowerCase() method of strings.

It returns a new string where all characters are lowercase.

Original string is not changed.


👉 Example:

let text = "HELLO WORLD";
let lower = text.toLowerCase();
console.log(lower); // "hello world"

✅ Definition: toLowerCase() is a string method that converts all characters in a string to lowercase.


---

43. What Is the Purpose of the map() Function in JavaScript?

map() is an array method.

It is used to transform each element of an array.

It creates a new array with the results.

It does not change the original array.


👉 Example:

let numbers = [1, 2, 3];
let doubled = numbers.map(n => n * 2);

console.log(doubled); // [2, 4, 6]

✅ Definition: map() is used to loop over an array and create a new array where each item is modified by a function.


---


