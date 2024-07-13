# Class Diagram for the Library Management System

Understand how to create a class diagram for a library management system by using the bottom-up approach.

> We'll cover the follwing:
>
> - Components of a library management system
>   > - Book and book item
>   > - Rack
>   > - Person and author
>   > - User, librarian, and library member
>   > - Library card
>   > - Book reservation
>   > - Book lending
>   > - Notification
>   > - Search and catalog
>   > - Library
>   > - Enumerations
>   > - Custom data type
> - Relationship between the classes
>   > - Association
>   >   > - One-way association
>   >   > - Two-way association
>   > - Composition
>   > - Aggregation
>   > - Inheritance
> - Class diagram of the library management system
> - Design pattern
> - Additional requirements

Create class diagram for our system on the basis of the requirements that we gathered previously.

In the class diagram, we will first design/create the classes, abstract classes, and interfaces for the system, and then we'll identify the relationship between classes in accordance with all requirements of the library management system.

## Components of a library management system

In this section, we will define the classes for LMS.  
 Since we follow bottom-up approach for designing a class diagram, we'll **first create the classes of small components.**  
 After that, we will **integrate those components and create the class diagram for the whole library management system.**

#### Book and book item

#### Rack

#### Person and author

#### User, librarian, and library member

#### Library card

#### Book reservation

#### Book lending

#### Notification

#### Search and catalog

#### Library

#### Enumerations

#### Custom data type

## Realtionship between the classes

### Association

##### One-way association

##### Two-way association

### Composition

### Aggregation

### Inheritance

## Class diagram for library management system

## Design patterns

- We can apply the **Factory design pattern to create objects and mandate that they go via a single factory.**  
   For example, we can create a BookFactory class to create a book object in an arranged manner.
- Similarly, we can use the **Delegation design pattern to delegate a task from one class to another class.**  
   For example, librarian functionalities like adding book items, deleting book items, or modifying book items are actually implemented in the BookItem class.  
   The Librarian class uses the BookItem class and has access to its data and methods.
- Moreover, we can use the **Observer design pattern to notify library members.**
  For example, if a member searched for a book that is unavailable at that time, then the observer interface system will notify the member when that bookis available for reservation.

## Additional Requirements
