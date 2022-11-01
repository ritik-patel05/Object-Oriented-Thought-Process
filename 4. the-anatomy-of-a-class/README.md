# the-anatomy-of-a-class

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
