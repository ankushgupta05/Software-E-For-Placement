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

Do you want me to also prepare **Q3 (What are Django’s advantages and disadvantages?)** in the same **easy style** to keep your set complete?
