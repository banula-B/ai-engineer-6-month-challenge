# Python Object-Oriented Programming (OOP) -- Complete Notes

## 1. What is OOP?

Object-Oriented Programming (OOP) is a programming paradigm that
organizes code into **objects**. An object contains both **data
(attributes)** and **behavior (methods)**.

### Why OOP?

-   Reusability
-   Modularity
-   Maintainability
-   Security through encapsulation
-   Easier real-world modeling

### Real-world analogy

A **Car** has: - Attributes: brand, color, speed - Methods: start(),
stop(), accelerate()

A class is the blueprint, while an object is the actual car.

------------------------------------------------------------------------

# 2. Class and Object

``` python
class Car:
    pass

car1 = Car()
car2 = Car()

print(type(car1))
```

A class defines structure. Every object created from it is called an
**instance**.

------------------------------------------------------------------------

# 3. Constructor (`__init__`)

The constructor runs automatically when an object is created.

``` python
class Car:
    def __init__(self, brand, color):
        self.brand = brand
        self.color = color

car = Car("Toyota", "Red")
print(car.brand)
print(car.color)
```

`self` refers to the current object.

------------------------------------------------------------------------

# 4. Attributes

## Instance attributes

``` python
class Student:
    def __init__(self, name):
        self.name = name
```

Each object has its own value.

## Class attributes

``` python
class Student:
    school = "ABC School"
```

Shared by all objects.

------------------------------------------------------------------------

# 5. Methods

``` python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        print(f"{self.name} says Woof!")
```

------------------------------------------------------------------------

# 6. The `self` Keyword

`self` represents the current object and lets methods access instance
attributes.

------------------------------------------------------------------------

# 7. Four Pillars of OOP

## Encapsulation

Hide internal data and control access.

``` python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance
```

Private attributes begin with `__`.

------------------------------------------------------------------------

## Abstraction

Hide implementation and expose only essential functionality.

``` python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

class Circle(Shape):
    def __init__(self, r):
        self.r = r

    def area(self):
        return 3.14 * self.r ** 2
```

------------------------------------------------------------------------

## Inheritance

``` python
class Animal:
    def speak(self):
        print("Animal sound")

class Dog(Animal):
    def bark(self):
        print("Woof")
```

Types: - Single - Multiple - Multilevel - Hierarchical - Hybrid

### `super()`

``` python
class Animal:
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)
        self.breed = breed
```

------------------------------------------------------------------------

## Polymorphism

``` python
class Dog:
    def speak(self):
        print("Woof")

class Cat:
    def speak(self):
        print("Meow")

for animal in [Dog(), Cat()]:
    animal.speak()
```

Method overriding:

``` python
class Animal:
    def speak(self):
        print("Sound")

class Dog(Animal):
    def speak(self):
        print("Woof")
```

------------------------------------------------------------------------

# 8. Special (Magic) Methods

``` python
class Book:
    def __init__(self, title):
        self.title = title

    def __str__(self):
        return self.title
```

Common methods: - `__init__` - `__str__` - `__repr__` - `__len__` -
`__eq__`

------------------------------------------------------------------------

# 9. Static and Class Methods

``` python
class Math:
    @staticmethod
    def add(a, b):
        return a + b

    count = 0

    @classmethod
    def increment(cls):
        cls.count += 1
```

------------------------------------------------------------------------

# 10. Composition

``` python
class Engine:
    def start(self):
        print("Engine started")

class Car:
    def __init__(self):
        self.engine = Engine()

    def start(self):
        self.engine.start()
```

------------------------------------------------------------------------

# 11. Example: Student Management

``` python
class Student:
    school = "ABC School"

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def display(self):
        print(self.name, self.marks)

    def is_pass(self):
        return self.marks >= 50

s1 = Student("Alice", 82)
s1.display()
print(s1.is_pass())
```

------------------------------------------------------------------------

# Summary

  Concept         Purpose
  --------------- -------------------------------
  Class           Blueprint
  Object          Instance of class
  Attribute       Data
  Method          Function inside class
  Constructor     Initializes object
  Encapsulation   Data hiding
  Abstraction     Hide complexity
  Inheritance     Reuse code
  Polymorphism    One interface, many behaviors
  `super()`       Call parent class
  Static Method   Utility method
  Class Method    Works with class
  Composition     Has-a relationship

These concepts form the foundation of Python OOP and are widely used in
real-world software development.
