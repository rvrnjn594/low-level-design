# Creational Design Patterns

Get introduced to creational design patterns and learn when to use them.

> We'll cover the following:
>
> - Introduction to creational design patterns
>   > - Factory pattern
>   > - Constructor pattern
>   > - Singleton pattern
>   > - Builder pattern
>   > - Prototype pattern
>   > - Abstract pattern

## Introduction to creational design patterns

Creational design pattern **deal with object creation mechanism.**

> - As the name implies, **_these patterns provide optimized object creation techniques._**
> - **_help cater to the design and complexity problems_** that might occur when using the basic approach.
> - also **_help control the creation of objects._**
>
> ![creational design pattern](./images/3-1-creational%20design%20pattern.png)

### Factory pattern

(provides a template that can be used to create objects.)  
 It is used in complex situations where the type of the object required varies and need to be specified in each case.

It does not use the _new_ keyword directly to instantiate objects.  
 This means that it doesn't explicitly require the use of constructor to create objects.  
 Instead, **it provides a generic interface that delegates the object creation responsibility to the corresponding subclass.**

### Constructor pattern

As the name defines, is a class-based pattern that **uses the constructors present in the class to create specific types of objects.**

### Singleton pattern

Type of design pattern that restricts the instantiation of a class to a single object.  
 This allows class to create its instance the first time it is instantiated.  
 However, on the next try, the existing instance of the class is returned. (no new instance is created.)

### Builder pattern

The Builder pattern is a type of a creational design pattern that helps in building complex objects using simpler objects.

> - It provides a flexible and step-by-step approach towards making these objects.
> - It also shields the representation and process of creation.

### Prototype pattern

The Prototype pattern is used to instantiate objects with some default values using an existing object.  
 It clones the object and provides the existing properties to the cloned object using prototypal inheritance.

> In **prototypal inheritance,** a prototype object acts as a blueprint from which other objects inherit when the constructor instantiates them.  
>  Hence, any properties defined on the prototype of a constructor function will also be present in the cloned object it creates.

### Abstract pattern

We use the Factory pattern to create multiple objects from the same family without having to deal with the creation process.  
 The Abstract Pattern is similar.

The differnce is that it provides a constructor to create families of related objects.  
 It is abstract, which means that it does not specify concrete classes or constructors.

## When to use creational design patterns?

- **Factory pattern:**
  - When the type of objects required cannot be anticipated beforehand.
  - When multiple objects that share similar characteristics need to be created.
  - When you want to generalize the object instantiation process, since the object set up is complex in nature.
- **Constructor pattern:**
  - When you want to create multiple instances of the same template, since the instances can share methods but can still be different.
  - It can be useful in the Libraries and Plugins design.
- **Singleton pattern:**
  - Where we want a single object to coordinate actions across a system.
  - **Services** can be singleton since they store the state, configuration, and provide access to resources. Therefore, it makes sense to have a single instance of a service in an application.
  - **Databases** such as MongoDB utilize the Singleton pattern when it comes to database concerns.
  - **Configurations** are used if there is an object with a specific configuration and we don't need a new instance every time that configuration object is needed.
- **Builder pattern:**
  - When building apps that require to create complex objects. It can help you hide the construction process of building these objects.
  - A good example would be DOM, where we might need to create plenty of nodes and attributes. The construction process can get quite messy if we are building a complex DOM object. In these cases, Builder pattern can be used.
- **Prototype pattern:**
  - To eliminate the overhead of initializing object.
  - When we want the system to be independent about how the products in it are created.
  - When creating objects from a database whose values are copied to the cloned object.
- **Abstract pattern:**
  - Applications requiring the reuse or sharing of objects.
  - Applications with complex logic because they have multiple families of related objects that need to be used together.
  - When we require object caching.
  - When the object creation process is to be shielded from the client.

> Let's look at the structural design pattern in the next lesson....
