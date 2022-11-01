# mastering-inheritance-and-composition

- Inheritance: involves inheriting attributes and behaviors from other classes, where there is a true parent/child relationship. The child (or subclass) inherits directly from the parent (or superclass).
- Composition: involves building objects by using other objects. involves using other classes to build more complex classes—a sort of assembly. No parent/child relationship exists in this case.
- Why? To reuse objects
- Relationship
  - is a: Inheritance (Child **is a** Parent)
  - behaves like(implements): Interfaces, you might add this.
    has a: Composition

## Inheritance

- It saves some design and coding time.
- It saves testing and maintenance time as well.
- E.g: Dog, Golden Retriver.
- The bark and pant methods are written only once and, assuming that they were properly tested when the Dog class was written, they do not need to be heavily tested again; but it does need to be retested because there are new interfaces, and so on.

### Problem is

gives a great example of a dilemma with design using inheritance. Consider a class for a bird. One of the most recognizable characteristics of a bird is, of course, that it can fly. So we create a class called Bird with a fly method. You should immediately understand the problem. What do we do with a penguin, or an ostrich? They are birds, yet they can’t fly. You could override the behavior locally, but the method would still be called fly. And it would not make sense to have a method called fly for a bird that does not fly but only waddles, runs, or swims.

“This is an example of the Liskov Substitution Principle of SOLID,”

In our dog example, we have designed the class so that all dogs have the ability to bark. However, some dogs do not bark. The Basenji breed is a barkless dog. Although these dogs do not bark, they do yodel. So should we reevaluate our design? What would this design look like? Figure 7.4 is an example that shows a more correct way to model the hierarchy of the Dog class.

Dog <- Barking Dog(barkEffiencieny, barks), Yodeling Dog (yodelFrequency, yodels)
Barking Dog <- LhasaApso (guardEfficiency, guards), GoldenRetriever (retrievalSpeed, retrieves)
Yodeling Dog <- Basenji(huntEfficieny, hunts)

Arrow in uml.

## Composition

- The classic example of object composition is the automobile.
- Diamond in uml.
- Model Complexity
As with the inheritance problem of the barking and yodeling dogs, using too much composition can also lead to more complexity. A fine line exists between creating an object model that contains enough granularity to be sufficiently expressive and a model that is so granular that it is difficult to understand and maintain.

In uml: Composition has aggregation and association.

## Example

- Dog is a Mammal, so the relationship is inheritance.
- Dog implements Nameable, so the relationship is an interface. (Dashed line represents interface)
- Dog has a Head, so the relationship is composition.

Now we can perform the true test of the interface. Is an interface an actual is-a relationship? The compiler thinks so:

``` java
Dog D = new Dog();
Nameable N = D;
```

This code works fine. So, we can safely say that a dog is a nameable entity. This is a simple but effective proof that both inheritance and interfaces constitute an is-a relationship. The interface relationship is more like a “behaves-like-a” when used properly. You might have data interfaces that are “is-a,” but more often you are going to have the former.

## Random

- The interface specifies behavior that is the same across classes that conceivably have no connection. Not only are dogs nameable, but so are cars, planets, and so on.
- Some say that interfaces are a poor substitute for multiple inheritance. While it may be true that interfaces were part of the same Java design that eliminated multiple inheritance (and were adopted by many other languages), interfaces are used in different design situations than inheritance, as the Nameable example illustrates.
