# Dictionaries and Classes – Student Notes

## 1. How Dictionaries and Classes Are Related

Both **dictionaries** and **classes** are used to **store related data about something**.

*   A **dictionary** stores data using **key–value pairs**
*   A **class** stores data using **attributes** and also stores **behaviour (methods)**

You can think of both as ways to model **real‑world objects**, such as a student, a game character or a bank account.

***

## 2. Using a Dictionary to Store an Object

A dictionary is often the **first step** students use to group related data.

### Example: Student stored as a dictionary

```python
student = {
    "name": "Alex",
    "age": 16,
    "year": 11
}

print(student["name"])
```

### What this does well

*   Groups related data together
*   Easy to create and understand
*   Useful for small programs or simple data storage

### Limitations

*   No built‑in behaviour (logic must be written separately)
*   No structure enforcement (keys can be misspelled)
*   Becomes hard to manage when programs get larger

***

## 3. Using a Class to Store an Object

A **class** is a blueprint for creating objects that contain:

*   **Attributes** (data)
*   **Methods** (functions that operate on the data)

This is a key idea in the **object‑oriented paradigm**, which students are required to study.

### Example: Student stored as a class

```python
class Student:
    def __init__(self, name, age, year):
        self.name = name
        self.age = age
        self.year = year

    def display_details(self):
        print(self.name, self.age, self.year)

student1 = Student("Alex", 16, 11)
student1.display_details()
```

***

## 4. Why Classes Are Better Than Dictionaries

### ✅ Reason 1: Classes Combine Data **and** Behaviour

With classes, data and the code that uses it are stored together.

**Dictionary approach**

```python
student["age"] += 1
```

**Class approach**

```python
class Student:
    def birthday(self):
        self.age += 1
```

This makes programs **easier to understand and maintain**.

***

### ✅ Reason 2: Classes Support Encapsulation

Encapsulation means **bundling data and methods together**, which reduces errors and improves code quality.

*   Dictionaries allow unrestricted access
*   Classes control how data is used

This is a core object‑oriented concept required by the syllabus.

***

### ✅ Reason 3: Classes Are Reusable and Scalable

Once a class is written, you can create **many objects** from it.

```python
student1 = Student("Alex", 16, 11)
student2 = Student("Sam", 17, 12)
```

Using dictionaries, each structure must be manually duplicated, increasing the chance of mistakes.

***

### ✅ Reason 4: Classes Enforce Structure

All objects created from a class have the **same attributes and methods**.

This:

*   Prevents missing data
*   Makes programs more predictable
*   Supports teamwork and larger projects

This aligns with professional software engineering practices introduced in Year 11.

***

## 5. When Dictionaries Are Still Useful

Dictionaries are still appropriate when:

*   Data is simple and temporary
*   Keys are not known in advance
*   You are storing configuration or lookup data

### Example: Lookup table

```python
grades = {
    "A": 90,
    "B": 80,
    "C": 70
}
```

***

## 6. Summary Table

| Feature                     | Dictionary | Class |
| --------------------------- | ---------- | ----- |
| Stores related data         | ✅          | ✅     |
| Stores behaviour            | ❌          | ✅     |
| Enforces structure          | ❌          | ✅     |
| Reusable                    | ❌          | ✅     |
| Suitable for large programs | ❌          | ✅     |

***

## 7. Exam‑Ready Summary Sentence

> Dictionaries store related data using key–value pairs, while classes store data and behaviour together, making classes more suitable for large, structured and maintainable software solutions.

