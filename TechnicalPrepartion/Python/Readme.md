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

👉 Do you want me to now combine **Q1 to Q10** into a clean **README.md interview Q\&A table format** for your notes?
