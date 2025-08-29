Okay 👍 I’ll keep the answers **very simple and easy to understand**.

---

### **Q2. What is the difference between Flask and Django?**

* **Flask**: A lightweight framework (you build most things yourself, more freedom, less built-in features).
* **Django**: A full-featured framework (comes with admin panel, authentication, ORM, etc. already built-in).

👉 Think: **Flask = small toolbox**, **Django = ready-made full house**.

---

### **Q4. What is the difference between a Project and an App?**

* **Project**: The whole website (contains settings, apps, database configs).
* **App**: A small part of the project (like blog, login system, payment, etc.).

👉 A **project can have many apps**.

---

### **Q5. Explain Django’s architecture.**

Django follows **MVT (Model-View-Template)** architecture:

1. **Model** – Handles database.
2. **View** – Handles logic (what to do when user requests something).
3. **Template** – Handles UI (HTML pages).

👉 Flow: **User request → View → Model → Template → Response**.

---

### **Q6. What are the Features of using Django?**

* Free and open-source.
* Built-in **Admin Panel**.
* **ORM** (easy database handling).
* **Security** features included.
* **Scalable** (can handle big projects).
* **Fast development** (many things already provided).

---

### **Q7. Explain the Django project directory structure.**

When you create a project, Django gives:

1. **manage.py** – Command-line tool for running the project.
2. **project\_name/** – Main folder.

   * **settings.py** – Project settings (database, apps, etc.).
   * **urls.py** – Routes (which page goes where).
   * **wsgi.py/asgi.py** – Server entry points.
   * **\_\_init\_\_.py** – Makes it a Python package.

👉 Apps you create will be inside the project.

---
Perfect 👍 Let’s do **Q7 – Django Project Directory Structure** in a **deep, complete, and very easy-to-understand way**. I’ll explain each file/folder one by one with examples so even a beginner can understand.

---

# ✅ Django Project Directory Structure

When you create a new Django project using:

```bash
django-admin startproject myproject
```

You get a folder like this:

```
myproject/
│
├── manage.py
│
├── myproject/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
```

Now let’s **explain each file**:

---

### 1️⃣ **manage.py**

* This is the command-line tool for your project.
* You use it to run the server, make migrations, create apps, etc.

👉 Example:

```bash
python manage.py runserver   # starts the development server
python manage.py makemigrations  # create migration files
python manage.py migrate     # apply migrations
python manage.py createsuperuser  # create admin user
```

So basically, **manage.py = the manager of your project**.

---

### 2️⃣ **myproject/ (inner folder)**

This is the **main configuration folder** for your project.
It contains important files that tell Django how your project works.

Inside it, we have:

---

#### 🔹 `__init__.py`

* This file makes the folder a **Python package**.
* Usually, it’s empty.
* Django just needs it so Python knows this folder contains code.

👉 Without this, Python will not treat it as a module.

---

#### 🔹 `settings.py`

* The **heart of your project**.
* It contains **all configurations/settings** of your Django project.

Some important settings inside:

* `INSTALLED_APPS`: List of apps in your project (like `auth`, `admin`, your custom apps).
* `DATABASES`: Defines which database you are using (SQLite, PostgreSQL, MySQL, etc.).
* `MIDDLEWARE`: Functions that process requests/responses (security, sessions, etc.).
* `TEMPLATES`: Where your HTML templates are stored.
* `STATIC_URL`: Path for static files (CSS, JS, images).

👉 Example (Database setting):

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / "db.sqlite3",
    }
}
```

So, **settings.py = project control room** 🚀.

---

#### 🔹 `urls.py`

* This file is like a **map of your website**.
* It connects **URLs → Views**.
* Example: when a user visits `/about`, Django checks here to know which view to call.

👉 Example:

```python
from django.contrib import admin
from django.urls import path
from . import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('about/', views.about_page),
]
```

So, **urls.py = traffic police (decides which request goes where)**. 🚦

---

#### 🔹 `asgi.py`

* Used for **Asynchronous Server Gateway Interface**.
* Needed if your project uses **WebSockets, real-time apps, async requests**.
* Mostly used in advanced cases (chat apps, live notifications).

👉 You rarely touch this file as a beginner.

---

#### 🔹 `wsgi.py`

* Used for **Web Server Gateway Interface**.
* It’s the entry point for **deployment** (when you host your project on a server).
* Example: Apache, Nginx, Gunicorn will use this file to start your project.

👉 For development, you don’t worry much, but in production, it’s very important.

---

# 🎯 Summary (Easy Remember)

* **manage.py** → Project manager (runs commands).
* ****init**.py** → Marks folder as a Python package.
* **settings.py** → Control room (all project settings).
* **urls.py** → Traffic police (routes requests).
* **asgi.py** → For async apps (real-time, WebSockets).
* **wsgi.py** → For deployment (server entry point).

---

⚡ So, whenever you start a Django project, these files are your **project backbone**.

---
Great 👍 Let’s go one by one in **easy and understandable language**.

---

## **Q 8. How do you create a Django project?**

👉 A **Django project** is the main container of your whole application.
It contains all apps, settings, and configurations.

### Steps:

1. Open terminal/command prompt.
2. Make sure Django is installed (`pip install django`).
3. Run the command:

   ```bash
   django-admin startproject projectname
   ```
4. This will create a folder with your **project files**.

✅ Example:

```bash
django-admin startproject myproject
```

Now a folder `myproject/` will be created with `manage.py` and settings files.

---

## **Q 9. How do you create a Django app?**

👉 A **Django app** is a module inside a project.
Each app does a specific task like **blog, accounts, payments, etc.**

### Steps:

1. Go to your project directory.
2. Run the command:

   ```bash
   python manage.py startapp appname
   ```
3. This will create a folder `appname/` with files like `views.py`, `models.py`, etc.

✅ Example:

```bash
python manage.py startapp blog
```

Now `blog/` app is created.

---

## **Q 10. How do we start our development server?**

👉 Django provides a built-in server for testing our project.

### Steps:

1. Go to the project folder (where `manage.py` is located).
2. Run the command:

   ```bash
   python manage.py runserver
   ```
3. Output will show something like:

   ```
   Starting development server at http://127.0.0.1:8000/
   ```
4. Open the link in a browser → Django project is running 🎉

---

## **Q 11. Importance of Virtual Environment setup for Django.**

👉 A **virtual environment** is like a separate box where your project’s Python libraries are installed.
👉 It avoids conflicts between multiple projects.

### Importance:

* Keeps **project dependencies separate**.
* Different projects can use **different versions** of Django or other libraries.
* Makes your project **easy to manage and portable**.

### Steps to create:

1. Install virtualenv:

   ```bash
   pip install virtualenv
   ```
2. Create environment:

   ```bash
   python -m venv env
   ```
3. Activate environment:

   * On Windows:

     ```bash
     env\Scripts\activate
     ```
   * On Mac/Linux:

     ```bash
     source env/bin/activate
     ```

✅ Now install Django inside it (`pip install django`).

---

Perfect 👍 Let’s go step by step with **very easy and deep explanations** for each question.

---

### ✅ Q 12. Give a brief about the Django admin interface.

👉 **Definition:**
The Django **admin interface** is a built-in web-based dashboard that Django provides for managing your database and models. It is automatically generated from your project’s models.

👉 **Explanation:**

* Once you create models in Django and register them inside `admin.py`, Django automatically shows them in the admin panel.
* It allows you to **add, update, delete, and search records** without writing SQL queries manually.
* You can also customize how models look and behave in the admin panel.

👉 **Steps to use:**

1. Create a superuser:

   ```bash
   python manage.py createsuperuser
   ```
2. Run the server:

   ```bash
   python manage.py runserver
   ```
3. Visit:

   ```
   http://127.0.0.1:8000/admin/
   ```

   → Login with the superuser credentials.

---

### ✅ Q 13. What are Django URLs?

👉 **Definition:**
A **URL (Uniform Resource Locator)** in Django defines the path (address) to a specific webpage or functionality.

👉 **Explanation:**

* Django uses a file called `urls.py` to **map URLs to views**.
* It decides what function (view) should run when a particular URL is requested.

👉 **Example:**

```python
# project/urls.py
from django.contrib import admin
from django.urls import path
from myapp import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('hello/', views.say_hello),  # when user visits /hello → say_hello() runs
]
```

---

### ✅ Q 14. What are the views of Django?

👉 **Definition:**
A **view** in Django is a Python function or class that takes a **web request** and returns a **web response** (HTML, JSON, etc.).

👉 **Explanation:**

* Views contain the **logic** of what should happen when someone visits a certain URL.
* They can fetch data from the database, process it, and send it to a template (HTML).

👉 **Example:**

```python
# myapp/views.py
from django.http import HttpResponse

def say_hello(request):
    return HttpResponse("Hello, Django World!")
```

---

### ✅ Q 15. What are the models in Django?

👉 **Definition:**
A **model** in Django is a **Python class** that defines the structure of your database table.

👉 **Explanation:**

* Each model maps to a **table** in the database.
* Each attribute inside the model is a **field** in the table.
* Django automatically creates SQL queries behind the scenes for you.

👉 **Example:**

```python
# myapp/models.py
from django.db import models

class Student(models.Model):
    name = models.CharField(max_length=100)
    age = models.IntegerField()
    email = models.EmailField()
```

➡️ This creates a database table like:

| id | name   | age | email                                     |
| -- | ------ | --- | ----------------------------------------- |
| 1  | Ankush | 21  | [ankush@test.com](mailto:ankush@test.com) |

---

### ✅ Q 16. What do the following commands do?

1️⃣ **`python manage.py makemigrations`**
👉 Creates migration files (blueprints of database changes).

* It looks at your models and prepares instructions on how to update the database.
* But it does **not** apply them yet.

2️⃣ **`python manage.py migrate`**
👉 Actually applies the migration files to the database.

* It creates or updates database tables according to your models.

👉 **Example Workflow:**

```bash
python manage.py makemigrations   # create migration file
python manage.py migrate          # apply it to DB
```

➡️ **Simple Example:**

* Add a new model `Student`.
* Run `makemigrations` → Django creates migration file.
* Run `migrate` → Table `Student` is created in DB.

---

Great questions 👌 Let’s go step by step in **simple words + examples** so that anyone can understand.

---

### ✅ Q21. Difference between **MVC** and **MVT** design patterns?

**MVC (Model–View–Controller)** → General web design pattern.
**MVT (Model–View–Template)** → Django’s design pattern (similar to MVC but a little different).

| MVC                                                   | MVT (Django)                                                                                 |
| ----------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| **Model** → Manages data & database.                  | **Model** → Same (handles database).                                                         |
| **View** → Displays data to user.                     | **Template** → Handles presentation (HTML, CSS).                                             |
| **Controller** → Controls logic (decides what to do). | **View** → Works like controller (contains business logic, fetches data, sends to template). |

👉 **Simple Example**
If user requests `/students/`:

* **Model** → Student table (data stored).
* **View (Django)** → Python function that fetches students from DB.
* **Template** → HTML file to show students.

So Django replaces **Controller** with its own **View**, and instead of **View**, it uses **Template**.

---

### ✅ Q22. What is Django ORM?

**ORM = Object Relational Mapper**

* It allows you to interact with the database using **Python code instead of raw SQL**.
* You don’t need to write `SELECT * FROM table...`, just use Python objects.

👉 **Example:**

```python
# models.py
from django.db import models

class Student(models.Model):
    name = models.CharField(max_length=100)
    age = models.IntegerField()
```

Now instead of SQL:

```sql
SELECT * FROM Student WHERE age=20;
```

We can use ORM in Python:

```python
students = Student.objects.filter(age=20)
```

✅ Easy, readable, and database-independent.

---

### ✅ Q23. What is Superuser?

* A **Superuser** is an admin user in Django with **all permissions**.
* Can **add, edit, delete, view** any data from the **Django Admin Panel**.
* Created using command:

```bash
python manage.py createsuperuser
```

👉 Example:

* Suppose you are building a school system.
* Superuser (`admin`) can manage **students, teachers, fees, results** from the admin dashboard without writing code.

---

📌 In short:

* **MVC vs MVT** → Django replaces Controller with View and View with Template.
* **ORM** → Write database queries in Python instead of SQL.
* **Superuser** → All-powerful admin user in Django.

---
Perfect 👍 Let’s go step by step with **deep but easy explanations** so that **anyone can understand clearly**.

---

## ✅ Q17. What are the sessions in Django?

👉 **Definition:**
A **session** in Django is a way to store information (data) about a specific user across multiple requests (pages).

* HTTP is **stateless**, meaning the server does not remember anything about the user between requests.
* **Sessions** help in storing data (like login info, cart items, preferences) so the server can "remember" the user.

👉 **How it works:**

* Django generates a **Session ID** (unique key).
* This ID is stored in the user's **browser cookie**.
* The actual session data is stored in the **database** (or cache, or file system).
* Whenever the user makes a request, Django checks the session ID and retrieves the data.

👉 **Example:**

```python
# views.py
def set_session(request):
    request.session['username'] = 'Ankush'
    return HttpResponse("Session set!")

def get_session(request):
    name = request.session.get('username')
    return HttpResponse(f"Hello, {name}")
```

* First view stores `"Ankush"` in session.
* Second view retrieves it later (even if you move to another page).

👉 **Uses:**

* Login system (storing user ID).
* Shopping cart (store items before checkout).
* User preferences (theme, language, etc.).

---

## ✅ Q18. Define static files and explain their uses.

👉 **Definition:**
**Static files** are the files that don’t change dynamically, such as:

* CSS (for styling)
* JavaScript (for frontend logic)
* Images, logos, fonts, etc.

👉 **Why needed:**

* They make your website look beautiful and interactive.
* Django provides a special system to manage and serve these files efficiently.

👉 **Example folder structure:**

```
project/
  app/
    static/
      css/
        style.css
      js/
        script.js
```

👉 **settings.py setup:**

```python
STATIC_URL = '/static/'
```

👉 **Usage in templates:**

```html
{% load static %}
<link rel="stylesheet" href="{% static 'css/style.css' %}">
<img src="{% static 'images/logo.png' %}" alt="Logo">
```

👉 **Uses:**

* Make the site attractive (CSS, images).
* Improve user experience (JavaScript).
* Keep project organized (separate static files from dynamic content).

---

## ✅ Q19. What are templates in Django?

👉 **Definition:**
A **template** in Django is an **HTML file with placeholders** (variables, tags, logic).

* Templates allow mixing **HTML + Django Template Language (DTL)**.
* They make webpages **dynamic** (content changes depending on data from backend).

👉 **Example template (home.html):**

```html
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>
<body>
    <h1>Welcome {{ name }}</h1>
    <p>Today is {{ date }}</p>
</body>
</html>
```

👉 **View (views.py):**

```python
from django.shortcuts import render
import datetime

def home(request):
    return render(request, 'home.html', {
        'name': 'Ankush',
        'date': datetime.date.today()
    })
```

👉 **Output on browser:**

```
Welcome Ankush
Today is 2025-08-29
```

👉 **Uses of templates:**

* Display data dynamically.
* Reuse design (same template for many users).
* Keep code clean (separating HTML from Python logic).

---

✅ In short:

* **Sessions** = Store user data across pages.
* **Static Files** = CSS, JS, Images for styling/interaction.
* **Templates** = HTML + Django Template Language to show dynamic content.

---



Here’s the continuation in the same simple **Q\&A format with examples** 👇

---

### ✅ Q 24. What is Jinja templating?

**Answer:**

* Jinja is a template engine used in Django (by default) for rendering HTML.
* It allows writing **dynamic HTML** by mixing Python-like syntax in templates.
* Example:

```html
<!-- templates/example.html -->
<h1>Hello, {{ name }}!</h1>
{% if age > 18 %}
    <p>You are an adult.</p>
{% else %}
    <p>You are a minor.</p>
{% endif %}
```

```python
# views.py
from django.shortcuts import render

def home(request):
    return render(request, "example.html", {"name": "Ankush", "age": 21})
```

✅ Output:

```
Hello, Ankush!
You are an adult.
```

---

### ✅ Q 25. What do you mean by the csrf\_token?

**Answer:**

* `csrf_token` stands for **Cross-Site Request Forgery token**.
* It is a **security measure** in Django to protect against malicious POST requests.
* When you submit a form, Django checks if the token is present and valid.

**Example:**

```html
<form method="POST">
    {% csrf_token %}
    <input type="text" name="username">
    <button type="submit">Submit</button>
</form>
```

🔐 Without `{% csrf_token %}`, Django will reject the POST request for security reasons.

---

### ✅ Q 26. Explain the use of Middlewares in Django.

**Answer:**

* Middlewares are **hooks** in Django’s request/response cycle.
* They sit **between the request and the response** and can process them.
* Example uses:

  * Authentication
  * Session management
  * Security checks (like CSRF, XSS protection)

**Example:**
Some default middlewares in `settings.py`:

```python
MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
]
```

➡️ Example: CSRF middleware checks every POST request for valid csrf\_token.

---

### ✅ Q 27. What are ‘signals’?

**Answer:**

* Signals are **Django’s way of sending notifications when something happens** in the project.
* Example: When a user is created, you may want to automatically create a profile for them.

**Example:**

```python
# signals.py
from django.db.models.signals import post_save
from django.contrib.auth.models import User
from django.dispatch import receiver
from .models import Profile

@receiver(post_save, sender=User)
def create_profile(sender, instance, created, **kwargs):
    if created:
        Profile.objects.create(user=instance)
```

➡️ Here, whenever a new `User` is saved, a `Profile` is automatically created.

---

Perfect 👍 Let’s cover them one by one in a **simple + example-based** way:

---

### ✅ Q28. What is Media Root?

* **Definition**:
  In Django, **Media Root** is the directory where **user-uploaded files** (like profile pictures, documents, etc.) are stored.

* **Settings Example** (`settings.py`):

  ```python
  MEDIA_URL = '/media/'   # URL to access media files
  MEDIA_ROOT = BASE_DIR / 'media'  # Folder inside project to store uploads
  ```

* **Usage Example** (`models.py`):

  ```python
  from django.db import models

  class Profile(models.Model):
      name = models.CharField(max_length=100)
      photo = models.ImageField(upload_to='profiles/')
  ```

  👉 Uploaded images will be saved in `media/profiles/`.

---

### ✅ Q29. How you can include and inherit files in your application?

* Django uses **Template Inheritance** (like HTML inheritance).

* **base.html** (parent template):

  ```html
  <!DOCTYPE html>
  <html>
  <head>
      <title>{% block title %}My Site{% endblock %}</title>
  </head>
  <body>
      <header>My Website Header</header>
      {% block content %}{% endblock %}
  </body>
  </html>
  ```

* **home.html** (child template):

  ```html
  {% extends 'base.html' %}

  {% block title %}Home Page{% endblock %}

  {% block content %}
      <h1>Welcome to Home Page</h1>
  {% endblock %}
  ```

👉 This avoids writing the same HTML code again and again.

---

### ✅ Q30. How do you connect your Django Project to the database?

* Configuration is done inside `settings.py`.

**Example (PostgreSQL):**

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'mydb',
        'USER': 'myuser',
        'PASSWORD': 'mypassword',
        'HOST': 'localhost',
        'PORT': '5432',
    }
}
```

👉 After setting this, run:

```bash
python manage.py migrate
```

to create tables in the database.

---

### ✅ Q31. Explain the caching strategies of Django.

* **Caching** = storing data temporarily so that future requests are faster.
* Django supports multiple caching strategies:

1. **File-based Cache**
   Stores cache data in files.

   ```python
   CACHES = {
       'default': {
           'BACKEND': 'django.core.cache.backends.filebased.FileBasedCache',
           'LOCATION': '/var/tmp/django_cache',
       }
   }
   ```

2. **Database Cache**
   Stores cache inside a database table.

   ```python
   CACHES = {
       'default': {
           'BACKEND': 'django.core.cache.backends.db.DatabaseCache',
           'LOCATION': 'my_cache_table',
       }
   }
   ```

3. **In-Memory Cache (LocMem)** – default, fastest for small projects.

   ```python
   CACHES = {
       'default': {
           'BACKEND': 'django.core.cache.backends.locmem.LocMemCache',
           'LOCATION': 'unique-snowflake',
       }
   }
   ```

4. **Memcached / Redis** – used in large projects for high performance.

👉 Example of caching in a view:

```python
from django.views.decorators.cache import cache_page

@cache_page(60 * 15)  # cache for 15 minutes
def my_view(request):
    return HttpResponse("This is cached data")
```

---

Great set of questions 👍 Let’s go one by one in **easy and deep explanation** so that anyone can understand.

---

## ✅ Q32. Give the exception classes present in Django

In Django, exceptions are special error classes that are raised when something goes wrong. They help developers handle errors gracefully.

### Common Exception Classes in Django:

1. **ObjectDoesNotExist** → Raised when a database query does not return any result.

   ```python
   from django.core.exceptions import ObjectDoesNotExist
   ```
2. **MultipleObjectsReturned** → Raised when a query that expects one object returns multiple.
3. **ValidationError** → Raised when data validation fails (e.g., form or model validation).
4. **PermissionDenied** → Raised when a user does not have permission to access something.
5. **SuspiciousOperation** → Raised for potentially dangerous operations (like wrong request headers).
6. **ImproperlyConfigured** → Raised when Django settings or configurations are wrong.
7. **FieldError** → Raised when there is an invalid field in queries or models.
8. **MiddlewareNotUsed** → Raised when middleware is not correctly loaded.

👉 These exceptions help in debugging and making web apps safe.

---

## ✅ Q33. What is NoSQL and Does Django support NoSQL?

### **NoSQL**:

* **NoSQL** = "Not Only SQL".
* It is a type of database that does not use traditional relational tables.
* Data is stored in different formats:

  * **Document-based** (MongoDB)
  * **Key-Value pairs** (Redis)
  * **Wide Column** (Cassandra)
  * **Graph databases** (Neo4j)

### **Does Django support NoSQL?**

* By default, Django supports **SQL databases only** (like PostgreSQL, MySQL, SQLite, Oracle).
* But, we can use **third-party libraries** for NoSQL:

  * **Djongo** → for MongoDB
  * **django-mongodb-engine** (older)
  * **django-redis** → for caching with Redis

👉 So Django is **not built for NoSQL by default**, but you can integrate NoSQL using external packages.

---

## ✅ Q34. What are the different model inheritance styles in Django?

In Django, model inheritance helps us reuse and organize database models better.

### Types of Model Inheritance:

1. **Abstract Base Classes**

   * Used when you want to put common fields in one parent class.
   * Parent table is **not created in database**.

   ```python
   class CommonInfo(models.Model):
       created_at = models.DateTimeField(auto_now_add=True)
       updated_at = models.DateTimeField(auto_now=True)
       class Meta:
           abstract = True

   class Student(CommonInfo):
       name = models.CharField(max_length=100)
   ```

2. **Multi-Table Inheritance**

   * Each model has its **own database table**.
   * Child table links to parent using **OneToOneField** automatically.

   ```python
   class Person(models.Model):
       name = models.CharField(max_length=100)

   class Student(Person):
       roll_no = models.IntegerField()
   ```

3. **Proxy Models**

   * No new table is created.
   * Just changes **Python-level behavior** (like adding extra methods).

   ```python
   class StudentProxy(Student):
       class Meta:
           proxy = True
       def welcome(self):
           return f"Welcome {self.name}"
   ```

👉 So Django supports **Abstract, Multi-table, and Proxy inheritance**.

---

## ✅ Q35. What databases are supported by Django?

By default, Django officially supports **Relational Databases (RDBMS)**:

1. **PostgreSQL** (Best supported)
2. **MySQL**
3. **SQLite** (Default for development)
4. **Oracle**

### Unofficial / Third-Party Database Support:

* **Microsoft SQL Server** (via `django-mssql-backend`)
* **MongoDB** (via Djongo or MongoEngine)
* **Redis** (used mainly for caching, not full DB)
* **Cassandra, CouchDB, Neo4j** (via third-party packages)

👉 So officially Django is **SQL-based**, but you can extend to NoSQL using packages.

---

📌 Would you like me to continue preparing **Q36–Q40** also in the same deep + easy way so you get a **full Django Interview Prep Set**?



