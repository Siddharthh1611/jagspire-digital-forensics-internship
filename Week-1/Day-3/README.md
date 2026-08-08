# Day 3 – Python Revision

## 🐍 Topics Covered

### 1. Variables & Data Types
Variables are used to store data.

**Examples:**
- int (10)
- float (10.5)
- string ("hello")
- boolean (True/False)

---

### 2. Functions
Functions are reusable blocks of code.

```python
def greet(name):
    return "Hello " + name
``` id="code1"

---

### 3. Object-Oriented Programming (OOP)

```python
class Person:
    def __init__(self, name):
        self.name = name

    def display(self):
        print("Name:", self.name)
``` id="code2"

---

### 4. File Handling

```python
with open("sample.txt", "w") as file:
    file.write("Hello World")
``` id="code3"

---

### 5. JSON Handling

```python
import json

data = {"name": "Siddharth", "role": "Intern"}

with open("data.json", "w") as f:
    json.dump(data, f)
``` id="code4"

---

### 6. APIs (requests module)

```python
import requests

response = requests.get("https://api.github.com")
print(response.status_code)
``` id="code5"

---

## 🧠 Key Learnings

- Python is essential for automation in digital forensics
- File handling helps in log analysis
- JSON is used for structured forensic data
- APIs help in integrating external tools

---

## 🚀 Status
Day 3 Completed Successfully
