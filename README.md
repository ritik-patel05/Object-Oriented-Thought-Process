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
    - If no constructor explicitly mentioned, default constructor always exists
    - Atleast one constructor always exists
- Multiple objects can be instantiated from a single class
- Each of these objects has a **unique** *identity* and *state*
- Methods: Represent *behaviours* of an object
- Attributes: Represent *state* of an object
- Operator Overloading
    - Enables us to change the meaning of an operator
    - Ex: + sign for strings can be overloaded to perform string concatenation
    - Ex: + for matrix, can perform matrix addition.
    - Be careful with it, it can be confusing. So document the logic so that people maintaining the code understand what is happening.
- Multiple Inheritance
    - To inherit from more than one class
    - It is a powerful technique, and some problems are difficult to solve w/o it.
    - In C++ we can, but not in Java, .NET, Swift(Bec. its complexity far outweighed its advantages)
- Object Operations:
    - Not easy to compare and copy an object.
    - Deep Copy: Must follow all references and create a new copy of all of them.
    - Class should have its own comparision method to compare itself.
    
 # The Anatomy of a Class
 
 - Name of Class
    - Info. about what the class does and how it interacts within larger systems.
 - Comments
 - Attributes
    Some keywords:
    - *private*: a method or variable can be accessed only within the declaring object.
    - *static*: one copy of this attribute for all objects instantiated by this class
 - Constructors
    - Coding no constructor and allowing the default constructor to be in play can cause  maintenance headaches down the road. If the code relies on a default constructor, and another constructor is added later, the default constructor will not be included by the system.
    - The Nothingness of Null
        - By setting the attribute to *null*(which is a valid condn.), we can check whether an attribute has been properly set.
        - Its always a good coding practice to initialize attributes in the constructors.
        - In the same vein, it’s a good programming practice to then test the value of an attribute to see whether it is null. 
    - Multiple Constructos
        - Less than ideal practice to use more than 1 constructor.
        - With the prevalence of Inversion of Control (IoC) containers and the like, it's frowned upon, and even unsupported, for a number of frameworks without special configuration.
- Accessors
    - A class should be very protective of its attributes. 
    - We dont want object A to inspect or change the attributes of B, without B having control. Why? *data integrity* and *efficient debugging*.
    - Also called getters and setters.
    - setters are used to ensure a level of data integrity.
- Public Interface Methods
- Private Implementation Methods

NOTE: Actually, there isn't a physical copy of each nonstatic method for each object. Each object would point to the same physical code. However, from a conceptual level, you can think of objects as being wholly independent and having their own attributes and methods.


# Class Design Guidelines

- Modeling Real-World Systems
    - Encapsulating the data and behaviour of a single entity. They are complete packages. A class should represent a logical component, such as taxicab.
- Identifying the Public Interfaces
    - Makes the class as concise as possible. 
    - If the public interface is not properly restricted, problems can result in the need for debugging, and trouble with system integrity and security.
    - Think of end users as customers! and we must satisfy their requirements.
- Designing Robust Constructors(and Destructors)
    - Constructor should put object into an initial, safe state. This includes issues such as attribute initialization and memory management.
- Designing Error Handling into a Class
- Designing with Reuse in Mind
    - Attempting to predict all the possible scenarios in which a object must operate.
- Designing with Extensibility in Mind
    - You would not want to code functionality into an Employee class that is specific to supervisory functions. If you did, and then a class that does not require supervisory functionality inherited from Employee, you would have a problem.
    - Keep scope as small as possible goes hand-in-hand with abstraction and hiding the implementation. The idea is to localize attributes and behaviors as much as possible.
- Designing with Maintanability in Mind
    - Separate pieces of code tend to be more maintainable than larger pieces of code
    - One of the best ways to promote maintainability is to reduce interdependent code—that is, changes in one class have no impact or minimal impact on other classes. * Highly Coupled Classes *
- Using Object Persistence

# Designing with Objects

1. Doing the proper analysis
2. Developing a statement of work that describes the system
3. Gathering the requirements from this statement of work
4. Developing a prototype for the user interface
5. Identifying the classes
6. Determine the responsibilities of each class
7. Determining how the various classes interact with each other
8. Creating a high-level model that describes the system to be built
    - Model: made up of class diagrams and class interactions. UML(Unified Modeling Language)

# Designing with Objects
    
