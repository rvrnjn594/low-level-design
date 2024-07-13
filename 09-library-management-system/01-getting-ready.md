# Getting Ready: Library Management System

Understand the library management system problem and learn the questions to simplify this problem.

> We'll cover the following:
>
> - Problem definition
> - Expectations from the interviewee
>
> > - Efficient searching
> > - Versatility
> > - Book reservation
> > - Book renewal
> > - Fine management
>
> - Design approach
> - Desing pattern

## Problem definition

A library management system (LMS) **aims to automate all library activities.** It is a **software that helps manage all the primary functions of library management.**  
 With the help of library management system, we can organize, handle, and maintain the record of numerous books and the members in a comprehensive and systematic way.

> - A librarian can use this software to track the number of books in the library. They can also use it to retain several records including, the new books, borrowed books with due dates, the member who borrowed books, returned books, fine on the returned books, etc.  
>   In short, **library management system stores and updates the complete library database.**
>
> - LMS also supports maintaining the physical library. The user can keep track of position of the book in the library and can search for whether or not the specific book is currently available in the library.  
>   Therefore, **LMS helps organize and retrieve library data in an efficient manner.**

## Expectations from the interviewee

There are multiple components of the LMS, each with its own specific requirements and constraints.

Let's look at some of the main expectations that the interviewer will want to hear you discuss in more detail during the interview.

### Efficient searching

Searching for books is one of the most crucial functions of LMS. The user must be able to search for any book.  
Different users may want to search for a book through different methods.

> Therfore, the interviewer can ask questions like these:
>
> - Would the user be able to search for a book using attributes other than the book name?
> - How will the user be able to search for a book by its author name, publication date, etc.?
> - How will the user search a specific category of books like magazines, journals, newspaper, etc.?

### Versatility

Before designing the system, it is mandatory to specify the actors of the system.

> Hence, the interviewer can ask about the actors of the system as follows:
>
> - Can the software only be used by a librarian or by all library members?

### Book reservation

Another significant feature of LMS is the reservation of the book.

> - What is mechanism of book reservation?
> - Can a member reserve a book again if it is already reserved?
> - How does the status of the book change when a member returns a book?

### Book renewal

> Similar to they book reservation, the interviewer can ask about the book renewal functionality with a question like this:
>
> - What is the mechanism of book renewal if a member wants to hold a book for a large period of time?

### Fine management

> There is another question that the interviewer may be interested to ask:
>
> - How is the calculation and deduction of fines handled if the book is returned late?

## Design approach

We are going to design this library system using the bottom-up design approach.

> For this purpose, we will follow the steps below:
>
> - Identify and design the smallest components first.
> - Use these small components to design bigger components.
> - Repeat the steps above until we design the whole system.s

## Design pattern

> During an interview, it is always a good practice to discuss the design patterns that a library management system falls under.
>
> Stating the design patterns give the interviewer a positive impression and shows that the interviewee is well-versed in the advanced concepts of object-oriented design.

---

> Let's explore the requirements of the library management system in the next lesson....
