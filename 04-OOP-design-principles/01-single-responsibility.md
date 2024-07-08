# SOLID: Single Responsibility Principle

Get familiar with the single responsibility principle aloing with its examples.

> We'll cover the following:
>
> - Introduction
> - Real-life example
> - Book invoice application
>   > - Violations
> - Conclusion

## Introduction

(perhaps the least understood of the SOLID concepts)  
Term coined by Robert C. Martin who defines the SRP as:  
 **_"A class should have only one reason to change."_**

> This implies that a class or component in our code should only have one functionality.  
>  (everything in class should be related to just one goal)

This helps in making modifications or adding extensions to the existing code much easier.

## Real-life example

> The following illustration represents how SRP is applied in real life:
> ![example of SRP](./images/01-SRP%20example.png)

## Book invoice application

Let's try to understand SRP with the help of example.

> We have a book invoice application that has two classes: Book and Invoice.  
>  The Book class contains data members related to the book, whereas th Invoice class contains three functinalities.
>
> Blueprint of these classes:
> ![class diagram of book invoice without applying SRP rule](./images/1-2-without%20SRP.png)
>
> > ### Violations
> >
> > Notice that the Invoice class violates the SRP in multiple ways:
> >
> > - The Invoice class is about invoices, but we have added print and storage functionality inside it.  
> >    This breaks the SRP rule, which states, "A class should have only one reason to change."
> > - If we want to change the logic of the printing or storage functionality in the future, we would need to change the class.
>
> Instead of modifying the Invoice class for these uses, we can create two new classes for printing and persistence logic: InvoicePrinter and InvoiceStorage, and move the methods accordingly, as shown below:
>
> ![class diagram after applying SRP rule](./images/1-3-after%20applying%20SRP.png)
>
> Now, our class structure is in line with the SRP.

## Conclusion

When a class performs one task, it contains a small number of methods and member variables that are self-explanatory.  
 SRP achieves this goal, and due to this, our classes are more usuable, and they provide easirt maintenance.

> In the next lesson, learn the Open Closed Design Principle with examples....
