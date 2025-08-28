Got it 👍 Here are **simple interview-style answers with explanations** for your questions:

---

### **1. Is Python a compiled language or an interpreted language?**

✅ **Answer:**
Python is an **interpreted language**.


### 🔍 Easy Explanation:

* In **compiled languages** (like C, C++): the whole program is translated first, then it runs.
* In **interpreted languages** (like Python): the program runs **line by line** as you write or test it.

👉 That’s why Python is called **interpreted**.


---

### **2. How can you concatenate two lists in Python?**

✅ **Answer:**
You can concatenate two lists using the **`+` operator** or the **`extend()` method**.

```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]

# Using +
result = list1 + list2   # [1, 2, 3, 4, 5, 6]

# Using extend()
list1.extend(list2)      # list1 becomes [1, 2, 3, 4, 5, 6]
```

🔍 **Explanation:**

* `+` creates a **new list**.
* `extend()` **modifies the existing list**.

---

### **3. Difference between for loop and while loop in Python**

✅ **Answer:**

* **for loop** → Used when you know the number of iterations.
* **while loop** → Used when you don’t know how many times to run, but depends on a condition.

```python
# For loop
for i in range(5):  
    print(i)   # runs 5 times (0 to 4)

# While loop
x = 0
while x < 5:
    print(x)
    x += 1
```

🔍 **Explanation:**

* **for loop** → Iterates over a sequence (list, range, string).
* **while loop** → Runs until the condition becomes **False**.

---

### **4. How do you floor a number in Python?**

✅ **Answer:**
Use the **`math.floor()`** function.

```python
import math

print(math.floor(4.7))   # 4
print(math.floor(-4.7))  # -5
```

🔍 **Explanation:**

* `floor()` means rounding down to the **nearest integer**.

---

### **5. What is the difference between `/` and `//` in Python?**

✅ **Answer:**

* `/` → **Floating-point division** (always returns decimal).
* `//` → **Floor division** (rounds down to nearest integer).

```python
print(5 / 2)   # 2.5
print(5 // 2)  # 2
print(-5 // 2) # -3 (floors towards negative infinity)
```

🔍 **Explanation:**

* `/` keeps decimals.
* `//` removes the decimal and floors the result.

---
Perfect 👍 I’ll write answers **in the same short & simple interview style** like before.

---

### **6. Is Indentation Required in Python?**

✅ **Answer:** Yes, indentation is required in Python.

🔍 **Easy Explanation:**

* Indentation means giving spaces before code.
* In Python, spaces decide the **block of code**.
* Without proper indentation, Python will show an **error**.

```python
if True:
    print("Hello")  # correct (indented)
```

---

### **7. Can we Pass a function as an argument in Python?**

✅ **Answer:** Yes, in Python a function can be passed as an argument.

🔍 **Easy Explanation:**

* Functions in Python are treated like **objects**.
* You can give a function **inside another function**.

```python
def greet(name):
    return f"Hello {name}"

def display(func):
    print(func("Ankush"))

display(greet)   # Output: Hello Ankush
```

---

### **8. What is a dynamically typed language?**

✅ **Answer:** Python is a **dynamically typed language**.

🔍 **Easy Explanation:**

* You **don’t need** to tell Python the type of variable.
* Python **decides automatically** at runtime.

```python
x = 10       # integer
x = "Hello"  # now string, no error
```

---

### **9. What is `pass` in Python?**

✅ **Answer:** `pass` means “do nothing.”

🔍 **Easy Explanation:**

* Sometimes you want to **keep code empty** but avoid errors.
* `pass` works like a **placeholder**.

```python
def my_func():
    pass   # no code yet
```

---

### **10. How are arguments passed in Python – by value or by reference?**

✅ **Answer:** In Python, arguments are passed **by object reference** (a mix of both).

🔍 **Easy Explanation:**

* If you change a **mutable object** (like list), changes affect the original.
* If it’s an **immutable object** (like int, string), it stays unchanged.

```python
def modify(lst):
    lst.append(100)

nums = [1, 2]
modify(nums)
print(nums)  # [1, 2, 100]  (changed because list is mutable)
```

---
Perfect 👍 I’ll make the **definitions a little longer and more descriptive** while keeping them **easy to understand**. Here’s Q11–Q15 updated:

---

### **11. What is a Lambda Function in Python and How to Use It?**

✅ **Answer:**
A **lambda function** is a **small anonymous function** in Python, which means it **does not need a name**. It is mainly used for **quick, simple operations** that can be written in a **single line**. Lambda functions are often used when passing a function as an argument to another function.

🔍 **Easy Explanation:**

* Think of it as a **shortcut** for creating a small function.
* Useful when you don’t want to define a full function using `def`.

```python
square = lambda x: x * x
print(square(5))   # 25
```

---

### **12. What is List Comprehension in Python? Give a Simple Example.**

✅ **Answer:**
**List comprehension** is a **concise way to create lists** in Python using a single line of code. It can replace **loops and multiple lines** of code, making the program cleaner and easier to read. You can also add conditions while creating the list.

🔍 **Easy Explanation:**

* Instead of writing multiple lines to create a list, you can **write one line** using list comprehension.
* Makes code **short and readable**.

```python
numbers = [x for x in range(5)]
print(numbers)   # [0, 1, 2, 3, 4]
```

---

### \*\*13. What are \*args and **kwargs in Python and How to Use Them?**

✅ **Answer:**

* `*args` allows a function to accept **any number of positional arguments**.
* `**kwargs` allows a function to accept **any number of keyword arguments** (key-value pairs).
  These features are useful when you **don’t know in advance** how many arguments will be passed to the function.

🔍 **Easy Explanation:**

* `*args` gives a tuple of all extra values passed.
* `**kwargs` gives a dictionary of all extra key-value pairs passed.

```python
def example(*args, **kwargs):
    print("args:", args)
    print("kwargs:", kwargs)

example(1, 2, 3, name="Ankush", age=22)

# Output:
# args: (1, 2, 3)
# kwargs: {'name': 'Ankush', 'age': 22}
```

---

### **14. What are break, continue and pass Statements in Python?**

✅ **Answer:**

* `break` **stops the loop completely**.
* `continue` **skips the current iteration** and moves to the next one.
* `pass` **does nothing**; it is used as a **placeholder** when code is required syntactically but you don’t want to execute anything.

🔍 **Easy Explanation:**

* `break` → use when you want to **exit a loop early**.
* `continue` → use when you want to **skip one step** but keep looping.
* `pass` → use when you plan to **write code later**.

```python
for i in range(5):
    if i == 2:
        continue   # skip 2
    if i == 4:
        break      # stop loop
    print(i)
# Output: 0, 1, 3
```

`pass` example:

```python
def my_func():
    pass   # code will be added later
```

---

### **15. Difference Between Set and Dictionary in Python with Examples**

✅ **Answer:**

* **Set** → a collection that stores **only unique values**. It does not allow duplicates and does not maintain any order.
* **Dictionary** → a collection of **key-value pairs**, where each key is unique and maps to a value.

🔍 **Easy Explanation:**

* Use a **set** when you need **unique items**.
* Use a **dictionary** when you need **pairs of data** that are easy to look up by key.

```python
# Set
my_set = {1, 2, 3, 3}
print(my_set)   # {1, 2, 3} (duplicates removed)

# Dictionary
my_dict = {"name": "Ankush", "age": 22}
print(my_dict["name"])   # Ankush
```

---

