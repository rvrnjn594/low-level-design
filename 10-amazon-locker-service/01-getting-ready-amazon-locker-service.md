# Getting Ready: Amazon Locker Service

Understand the Amazon Locker service problem and learn the questions to further this problem.

> We'll cover the following:
>
> - Problem definition
> - Expectations from the interviewee
>   - Locker size
>   - Locker selection
>   - Locker status
>   - Returning an item
> - Design approch
> - Design pattern

## Problem definition

**Amazon** is an online retail platform that allows its customers to place orders and buy products online. There are times when the customer is not available in the particular location to pick up the order.  
 In such a case, Amazon Locker can be one of the most secure way of delivery.

Amazon Locker is also known as Amazon Hub or Amazon Hub Locker.  
 It is a fully automated package delivery service provided by Amazon.  
 Customers can choose any locker location as their delivery address and pick up the package from that location at no additional cost.  
 In particular, when a customer places an order and chooses to get their item delivered to locker service, the system suggests the nearest available locker based on preferences. The order is packaged and placed in the locker. The customer gets the notification containing the code to open the locker, and they can pick up the package using that code within a valid amount of time.  
 This is how Amazon Locker service functions.

The problem is applicable to any retailer who wants to deliver goods safely to their customers.

## Expectations from the interviewee

The Amazon Locker service consists of multiple components. Each component has its own functionality and constraints.  
The following section provides an overview of some of the main expectations that the interviewer will want to hear you discuss in more detail during the interview.

#### Locker size

**Every locker is of specific size in the Amazon Locker system.**

> The interviewer expects you to ask questions listed below:
>
> - Will every locker be of the same size?
> - Is there any size restriction on an item that can be kept in the locker?

#### Locker selection

The most significant part of the Amazon Locker service is the selection of the locker.  
The system has to make sure that more than one customer should not be able to access a locker at a single time.

> The interviewer expects you to ask the questions listed below to identify how the system will work in such situations:
>
> - How will the system make sure that multiple customers do not get the same locker?
> - Will the customer choose the locker of his own choice, or will the system assign him a locker based on availability?
> - Can a customer get two lockers for different orders at the same time?
> - Will the system keep in mind the locker and package sized while assigning the locker to customer?

#### Locker status

Since this problem revolves around the locker, you may ask the questions listed below about the locker status:

> - Is there any time constraints on the package that can be kept in the locker?
> - What will happen if the customer does not come to pick up his package within the valid time period?

#### Returning an item

Similar to the order delivery process, the item can also be returned through the Amazon Locker service.

> Therefore, you may ask the questions listed below:
>
> - Can the customer return an item through the Amazon Locker service?
> - If yes, will they get the same locker from which they picked up the item?
> - How will the locker be assigned to the customer while returning an item?

## Design approach

We will design this Amazon Locker service using the bottom-up design approach.

> For this purpose, we will follow the steps below:
>
> - Identify and design the simple components first, like the locker and item.
> - Use these small components to design bigger components, such as the locker location and order that can be composed of multiple locker and items, respectively.
> - Repeat the steps above until we design the whole system.

## Design pattern

During an interview, it is always a good practice to discuss the design patterns that the amazon locker system falls under.  
 Stating the design patterns gives the interviewer a positive impression and shows that the interviewee is well-versed in the advanced concepts of object-oriented design.

> Sure, here are the design patterns that would be appropriate for designing an Amazon Locker service:
>
> 1. **Singleton design pattern:** This pattern ensures that there is only one instance of the Amazon Locker Service, which is globally accessible. This prevents unnecessary duplication and provides a central point of control.
> 2. **Factory design pattern:** This pattern is used to create different types of lockers with a consistent interface. This allows for flexibility and adaptability in meeting varying demands.
> 3. **Command design pattern:** This pattern encapsulates requests for locker operations as objects. This supports the queuing, logging, and asynchronous execution of commands.
> 4. **Observer design pattern:** This pattern enables a notification system for users by establishing a one-to-many dependency between lockers and interested observers. This ensures timely updates on locker status.
> 5. **Strategy design pattern:** This pattern defines interchangeable algorithms for locker selection and management. This allows dynamic selection based on specific user preferences or system conditions.
> 6. **State design pattern:** This pattern models different states of lockers and facilitates smooth transitions between states. This makes it easier to manage and represent the lifecycle of a locker.
> 7. **Decorator design pattern:** This pattern dynamically adds or alters features of lockers. This provides a flexible way to extend functionality without modifying the core structure of the locker service.
> 8. **Composite design pattern:** This pattern structures lockers hierarchically, allowing the composition of lockers into larger units. This is beneficial for managing groups of lockers with a unified interface.
> 9. **Proxy design pattern:** This pattern establishes a chain of handlers for processing locker-related requests. This allows for the decoupling of senders and receivers and provides flexibility in handling various requests.
> 10. **Template Method design pattern:** This pattern controls access to lockers through a proxy. This facilitates the implementation of additional security measures, logging, or performance optimizations without modifying the locker service.

Let's explore the requirements of the Amazon Locker service in the next lessson.
