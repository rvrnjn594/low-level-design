# Encapsulation

Get familiar with important aspects of object-oriented programming called **data hiding and encapsulation.**

> We'll cover the following:
>
> - Data hiding
> - Components of data hiding
> - Encapsulation
>   > - Implementing encapsulation in programming language
>   > - Advantages of encapsulation

## Data hiding

Data hiding (essential concept in object-oriented programming), defined as **masking a class's internal operations and only providing an interface through which other entities can interact with the class without being aware of what is happening within.**

The goal is to implement classes in a way that prevents unauthorized access to or modification of the original contents of a class by its instances (or created objects).

The underlying algorithms of one class need not be known to another class. The two classes can still communicate, though.

## Components of data hiding

Data hiding can be divided into two primary components:

- Encapsulation
- Abstraction
  (When used together, they allow us to make efficient classes for further use in our application.)

## Encapsulation

(fundamental programming technique used to achieve data hiding in OOP)  
Encapsulation is OOP refers to **binding data and the methods to manipulate that data together in a single unit - class.**

Encapsulation is usually done to hide the state and representation of an object from the outside world.  
_(A class can be thought of as a capsule with methods and attributes inside it.)_

> When encapsulating classes, a good convention is to declare all variables of a class private. This restrict direct access by the code outside that class.
>
> If the methods and variables are encapsulated in a class, how can they be used outside that class?
>
> > One has to implement public methods to let the outside world communicate with this class.  
> > These methods are called **getters and setters.**

The private members (variables or functions) cannot be accessed directly from the outside world, but public read and write functions allow access to them. This, in essence, is **data encapsulation.**

## Advantages of encapsulation

- Classes are simpler to modify and maintain.
- Which data members we wish to keep hidden or accessible can be specified.
- We choose which variables are read-only and write-only (increases flexibility).

> In the next lesson, we discuss the concept of abstraction...
