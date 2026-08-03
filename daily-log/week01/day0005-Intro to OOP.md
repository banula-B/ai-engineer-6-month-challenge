# Introduction to Object-Oriented Programming (OOP)

Object-Oriented Programming (OOP) is a paradigm in software development
that helps developers manage complexity by organizing code into
**classes** and **objects**. It allows you to model real-world items and
their behaviors directly within your software.

### The Core Concepts

-   **Classes and Objects**: Think of a **Class** as a blueprint (like
    an architectural drawing for a house). An **Object** is the actual
    thing built from that blueprint (the physical house). You define
    attributes (data like size or color) and methods (actions like 'open
    door' or 'turn on lights') inside the class.
-   **Constructor (`__init__`)**: This is a special setup method. When
    you create a new object from your blueprint, the `__init__` method
    runs automatically to give that object its starting data, ensuring
    it is ready for use immediately.
-   **Methods**: These are essentially functions that live inside a
    class. They use the `self` keyword to refer to the specific object
    they are currently working with, allowing them to manipulate the
    data of that individual instance.

### The Four Pillars of OOP

1.  **Encapsulation**: This involves keeping data safe by restricting
    direct access. You hide the internal details and only allow
    modifications through specific methods, which prevents data from
    being accidentally corrupted.
2.  **Abstraction**: This principle focuses on showing only what is
    necessary to the user. You hide the complex, behind-the-scenes logic
    so the user only sees a simple, easy-to-use interface.
3.  **Inheritance**: This allows you to create new classes based on
    existing ones. If you have a general `Item` class, you can create a
    specific `Phone` class that automatically inherits all the features
    of `Item`, plus its own unique traits. This promotes code reuse.
4.  **Polymorphism**: This is the ability for a single command to work
    differently depending on the object. For example, a
    `calculate_price()` method might work one way for a *Phone* and
    another way for a *Keyboard*, even though both objects respond to
    the same command name.
