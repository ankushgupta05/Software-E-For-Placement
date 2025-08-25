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

37. Explain the Concept of Event Bubbling in JavaScript.

Event Bubbling means when an event happens on a child element, it moves upward (bubbles) through its parent elements.

The event is first handled by the target element, then by its parent, then by the ancestor elements, up to the root.


👉 Example:
Clicking a button inside a <div> will first trigger the button’s click, then the <div>’s click, and so on.


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

