# Employee Management System (Abstraction)

## Project Overview

The Employee Management System is a Python project developed using Object-Oriented Programming (OOP) concepts, with a primary focus on **Abstraction**.

The project demonstrates how different types of employees can perform different tasks while following a common structure defined by an abstract base class.

This project was developed as part of my Data Science and Machine Learning learning journey.

---

## Features

### Employee Information

Stores employee details such as:

* Name
* Age
* Salary

---

### Developer Management

Stores additional information:

* Programming Language
* Field of Expertise

Example:

```text
Language: Python
Field: Data Science
```

Work Performed:

```text
Writing Python Code
```

---

### Tester Management

Stores testing-related information:

* Testing Tool

Example:

```text
Tool: Selenium
```

Work Performed:

```text
Testing software using Selenium
```

---

### Manager Management

Stores management-related information:

* Department

Example:

```text
Department: IT
```

Work Performed:

```text
Managing IT Department
```

---

## OOP Concepts Used

### Class

```python
class Employee
```

Acts as the parent class for all employee types.

---

### Object

```python
dev = Developer(...)
test = Tester(...)
manager = Manager(...)
```

Objects represent real employees.

---

### Constructor

```python
def __init__()
```

Used to initialize employee details when objects are created.

---

### Inheritance

```python
class Developer(Employee)
class Tester(Employee)
class Manager(Employee)
```

All child classes inherit common properties from the Employee class.

---

### Method Overriding

Each child class provides its own implementation of:

```python
work()
```

Example:

```python
Developer → Writing Code

Tester → Testing Software

Manager → Managing Department
```

---

### Polymorphism

The same method:

```python
work()
```

produces different outputs depending on the object calling it.

Example:

```python
for emp in employees:
    emp.work()
```

---

### Abstraction

Implemented using:

```python
from abc import ABC, abstractmethod
```

The abstract method:

```python
@abstractmethod
def work(self):
    pass
```

forces all child classes to implement their own version of the `work()` method.

---

## Project Structure

```text
Employee (Abstract Class)
│
├── name
├── age
├── salary
│
├── show_details()
└── work() [Abstract Method]

        ▲
        │
 ┌──────┼──────┐
 │      │      │
 ▼      ▼      ▼

Developer  Tester  Manager
```

---

## Sample Output

```text
Name: Jaydeep
Age: 21
Salary: 50000
Language: Python
Field: Data Science

Work: Writing Python Code

______________________________

Name: Bhumi
Age: 21
Salary: 25000
Tool: Selenium

Work: Testing software using Selenium

______________________________

Name: Shantanu
Age: 25
Salary: 40000
Department: IT

Work: Managing IT Department
```

---

## Technologies Used

* Python
* Object-Oriented Programming (OOP)
* Abstract Base Classes (ABC)

---

## Learning Outcomes

Through this project, I learned:

* Abstract Classes
* Abstract Methods
* Abstraction
* Inheritance
* Method Overriding
* Polymorphism
* Constructor Chaining using `super()`
* Code Reusability
* Object-Oriented Design

---

## Real-World Applications

The concepts used in this project are commonly found in:

* Employee Management Systems
* Human Resource Management Software
* Enterprise Applications
* Company Payroll Systems
* Organizational Management Platforms

---

## Future Improvements

* Employee ID System
* Department Management
* Attendance Tracking
* Salary Calculation
* Promotion Management
* Database Integration
* File Handling Support
* GUI Version using Tkinter

---

## Repository Structure

```text
employee-management-system-abstraction/
│
├── employee_management_system.py
├── README.md
└── screenshots/
```
