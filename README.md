# Object-Oriented-Thought-Process
Learnings from book, Object-Oriented Thought Process, 5th Edition by Matt Weisfeld

# Introduction to Object-Oriented Concepts

**Encapsulation** — Encapsulating the data and behavior into a single object is of primary importance in OO development. A single object contains both its data and behaviors and can hide what it wants from other objects.

**Inheritance(is-a)** — A class can inherit from another class and take advantage of the attributes and methods defined by the superclass.
Ex: Cat *is-a* Mammal, Dog *is-a* Mammal

**Polymorphism** — Polymorphism means that similar objects can respond to the same message in different ways. For example, you might have a system with many shapes. However, a circle, a square, and a star are each drawn differently. Using polymorphism, you can send each of these shapes the same message (for example, Draw), and each shape is responsible for drawing itself.

**Composition(has-a)** — Composition means that an object is built from other objects.
Ex: a computer *has-a* video card, *has-a* keyboard, and *has-a* disk drive

# How to Think in Terms of Objects

- Knowing the Difference Between the Interface and the Implementation
- Using Abstract Thinking When Designing Interfaces
    - Who are users of this object,
    - What functionality they require?
- Providing the Absolute Minimal User Interface Possible
    - Starting with no methods is better than providing more methods to user

# More Object Oriented Concepts

- Constructors
    - When they are called? -> When a new object is created.
    - Job:
        - To initialize the memory
        - To call the constructor of its superclass.
    - If no constructor explicitly mentioned, default constructor is always exists
    - Atleast one constructor always exists
- Multiple objects can be instantiated from a single class
- Each of these objects has a **unique** *identity* and *state*
- Methods: Represent *behaviours* of an object
- Attributes: Represent *state* of an object
- Operator Overloading
- Multiple Inheritance
- Object Operations:
    - Not easy to compare and copy an object.
    - Deep Copy: Must follow all references and create a new copy of all of them.
    - Class should have its own comparision method to compare itself.