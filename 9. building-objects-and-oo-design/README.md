# building-objects-and-oo-design

## Composition

- Another major advantage in using composition is that systems and subsystems can be built independently, and perhaps more importantly, tested and maintained independently.

## Types of Composition

- An aggregation is a complex object composed of other objects. An association is used when one object wants another object to perform a service for it.

### Examples

- Consider that an Employee object might be composed of an Address object and a Spouse object. You might consider the Address object as an aggregation (basically a part of the Employee object), and the Spouse object as an association. To illustrate, suppose both the employee and the spouse are employees. If the employee is fired, the spouse is still in the system but the association is broken.

- In the car example, although the engine, spark plugs, and doors represent composition, the stereo also represents an association relationship. In reality, cars and desktop computers are a mix of aggregations and associations.

- Relationship b/w Dog and Owner: Association. The owner is clearly not part of the dog, or vice versa, so we can safely eliminate aggregation.

## Cardinality

To determine cardinality, answer this questions.

1. Which objects collaborate with which other objects?
2. How many objects participate in each collaboration?
3. Is the collaboration optional or mandatory?

## Cardinality of Class associations
Optional/Association - Cardinality - Mandatory
Employee/Division - 1 - Mand.
Employee/JobDescription - 1..n - Mand.
Employee/Spouse - 0..1 - Optional.
Employee/Child - 0..n - Optional.

- Cardinality Notation
The notation of 0 . . 1 means that an employee can have either zero or one spouse. The notation of 0 . . n means that an employee can have any number of children from zero to an unlimited number. The n basically represents infinity.

- Note that the classes that have a one-to-many relationship are represented by arrays in the code.

### Optional Associations
- One of the most important issues when dealing with associations is to make sure that your application is designed to check for optional associations. This means that your code must check to see whether the association is null.
- For example, if no spouse exists, the code must not attempt to invoke a spouse behavior. This could lead to an application failure. Thus, the code must be able to process an Employee object that has no spouse.
