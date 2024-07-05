# Inheritance

Get familiar with the concept of inheritance and its type with implementation.

> We'll cover the following:
>
> - Definition
> - The IS-A relationship
> - Modes of inheritance
> - Types of inheritance
>   > - Single inheritance
>   > - Multiple inheritance
>   > - Multi-level inheritance
>   > - Hierarchical inheritance
>   > - Hybrid inheritance
> - Implementation
> - Advantages of inheritance

## Definition

**Inheritance** provides a way to create a new class from an existing class.  
The new class is a specialized version of the existing class such that it inherits all the public attributes (variables) and methods of the existing class.  
The existing class is used as a starting point or base to create the new class.

## The IS-A relationship

Whenever we come across an IS-A relationship between objects, we can use inheritance.

Remember, we cannot use inheritance if an IS-A relationship doesn't exist between classes.

## Modes of inheritance

**Access modifiers** are tags we can associate with each member to define the parts of the program they can access directly.

By using these modifiers, we define the scope of the data members and member functions for the other classes and main.

## Types of inheritance

Based on parent classes and child classes, there are five types of inheritance in general:

- Single:  
  there is only a single class extending from a single parent class. eg: a fuel car IS-A vehihcle.
- Multiple:  
  when a class is derived from more than one base class, ie., when a class has more than one immediate parent class, it is called multiple inheritance. eg: the hybrid IS-A fuel car, the hybrid IS-A electric car as well.
- Multi-level:  
  when a class is derived from a class that itself is derived from another class, it is called multi-level inheritance. eg: a fuel car IS-A vehicle, a gasoline car IS-A fuel car.
- Hierarchical:  
  In hierarchical inheritance, more than one class extends, as per the requirement of the design, from the same base class. The common attributes of these child classes are implemented inside the base class. eg: a fuel car IS-A vehicle, an electric car IS-A vehicle.
- Hybrid:  
  A type of inheritance that is combination of more than one type of inheritance is called **hybrid inheritance.** eg: a fuel car IS-A vehicle, an electric car IS-A vehicle, a hybrid car IS-A fuel car and IS-A electric car.

## Implementation

> **NOTE:** Some languages, such as JAVA, C# and Javascript, do not support multiple inheritance through classes.

## Advantages of inheritance

Four main advantages of inheritance:

- Reusability:  
  don't need to duplicate methods inside the child classes that also occur in the parent classes.
- Code modification:  
  ensures that all changes are localized and inconsistencies are avoided.
- Extensibility:  
  can extend the base class as per the requirements of the derived class. Provides an easy way to upgrade or enhance specific parts of a product without changing the core attributes.
- Data hiding:  
  a base class can keep some data private so that the derived class cannot alter. This concept is called **encapsulation.**

> Let's learn about polymorphism in next lesson....
