Got it 👍 Here are **simple interview-style answers with explanations** for your questions:

---

### **1. Is Python a compiled language or an interpreted language?**

✅ **Answer:**
Python is an **interpreted language**.

🔍 **Explanation:**

* Python code is first compiled into **bytecode** (intermediate form).
* Then, the **Python interpreter (PVM – Python Virtual Machine)** executes this bytecode line by line.
* So, Python is not purely compiled like C/C++ and not purely interpreted either, but mostly considered **interpreted**.

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

👉 Do you want me to put these in a **README.md interview Q\&A table format** (like the style we used earlier), so you can directly keep it as notes?

