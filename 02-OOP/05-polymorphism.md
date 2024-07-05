# Polymorphism

Get familiar with the concept of polymorphism and its types with implementation.

> We'll cover the following:
>
> - Introduction to polymorphism
> - Types of polymorphism
>   > - Dynamic polymorphism
>   >   > - Method overriding
>   > - Static polymorphism
>   >   > - Method overloading
>   >   > - Operator overloading
>   > - Dynamic polymorphism vs. static polymorphism

## Introduction to polymorphism

(combination of two Greek words, "poly" meaning many, and "morph" meaning forms.)  
In programming, polymorphism is a phenomenon that allows an object to have several different forms and behaviors.

## Types of polymorphism

There are two types of polymorphism: dynamic polymorphism and static polymorphism, as shown:
![types of polymorphism](./images//types%20of%20polymorphism.png)

### Dynamic polymorphism

Dynamic polymorphism is the mechanism that **defines the methods with the same name, return type, and parameters in the base class and derived classes.**  
Hence, the call to overridden method is decided at runtime.

> This is why dynamic polymorphism is also know as **runtime polymorphism**. It is achieved by method overriding.

#### Method overriding

In object-oriented programming, if a subclass provided a specific implementation of a method that had already been defined in one of its parent classes, it is known as **methid overrding.**

### Static polymorphism

Static polymorphism is also known as **compile-time polymorphism**, and it is achieved by **method overloading or operator overloading.**

#### Method overloading

Methods are said to be overloaded if a class **has more than one method with the same name,** _but either the number of arguments is different, or the type of arguments is different._

#### Operator overloading

Operators can be overloaded to operate in a certain user-defined way.  
Its corresponding method is invoked to perform its predefined function whenever an operator is used.

> **Note:** Java and JavaScript do not support operator overloading.

### Dynamic polymorphism vs. Static polymorphism

Static Polymorphism:

- Polymorphism that is resolved during compile-time is known as static polymorphism.
- Method overloading is used in static polymorphism.
- Mostly used to increase the readability of the code.
- Arguments must be different in the casr of overloading.
- **Return type of the method does not matter.**
- Private and sealed methods can be overloaded.
- Gives a better performance because the binding is being done at compile-time.

Dynamic Polymorphism:

- Polymorphism that is resolved during runtime is known as dynamic polymorphism.
- Method overriding is used in dynamic polymorphism.
- Mostly used to have a seperate implementation for a method that is already defined in the base class.
- Arguments must be the same in the case of overriding.
- Return type of the method must be the same.
- Private and sealed methods cannot be overridden.
- Gives worse performance because the binding is being done at runtime.

> End of OOP chapter.
