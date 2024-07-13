# Sequence Diagram for the Library Manegement System

Create a sequence diagram for lending a book from the library and solve a challenge.

> We'll cover the following:
>
> - Issue a book
> - Return a book

Sequence diagrams are a great way to understatnd the interactions between different entitites and objects in the system.

There can be different sequence diagrams that we can create for our library management system. For the sake of this lesson, we will create sequence diagrams for the following two interactions:

- **Lend a book:**  
   The member requests the librarian to lend them a book.
- **Return a book:**  
   The member returns a book.

## Issue a book

> The sequence diagram for issuing a book should have the following actors and objects that will interact with each other.
>
> - **Actors:** Member and Librarian
> - **Object:** Book

Here are the steps in the sequence to issue a book:

1. The member requests to isssue a book.
2. The librarian verifies the lending quota of the member.
3. If the lending quota is equal to the maximum quota:
   - The librarian informs the member that the maximum quota is reached. No more books can be issued.
4. Else if the lending quota is less than the maximum quotaL
   - The librarian gets the book status.
   - If the book is available:
     - The librarian issues the book to the member.
   - If the book is reserved:
     - The librarian cancels the member's request to issue the book.

Based on the order above, the sequence diagram below demonstrates the issuance of a book in the library management system.
