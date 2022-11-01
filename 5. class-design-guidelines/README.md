# class-design-guidelines

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
  - One of the best ways to promote maintainability is to reduce interdependent code—that is, changes in one class have no impact or minimal impact on other classes. *Highly Coupled Classes*
- Using Object Persistence
