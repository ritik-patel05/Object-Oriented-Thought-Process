# frameworks-and-reuse

we focus on using interfaces and abstract classes to create frameworks and encourage reusable code.

## What is a Framework?

- Hand in hand with the concept of code reuse is the concept of **standardization**, which is sometimes called **plug and play**. The idea of a framework revolves around these **plug-and-play** and **reuse principles**.

## Contract

we will consider a contract to be any mechanism that requires a developer to comply with the specifications of an API. Often, an API is referred to as a framework

## Abstract Classes

- An abstract class is a class that contains one or more methods that do not have any implementation provided. Suppose that you have an abstract class called Shape.

Implements a Contract:::
In C++: Abstract class
In Java, .NET: Interface

For example, the following C++ code is an abstract class. However, because the only method in the class is a virtual method, there is no implementation.

class Shape
{
    public:
        virtual void draw() = 0;
}

## Interface

- In the code, notice that Nameable is not declared as a class but as an interface. Because of this, both methods, getName() and setName(), are considered abstract and no implementation is provided.
- An interface, unlike an abstract class, can provide no implementation at all.
- As a result, any class that implements an interface must provide the implementation for all methods.

## Abstract Classes vs Interface

- an abstract class can provides both abstract and concrete methods, whereas an interface provides only abstract methods.
