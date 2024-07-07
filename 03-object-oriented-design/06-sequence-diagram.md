# Sequence Diagram

Understand how sequence diagrams represent interactions between actors and objects.

> We'll cover the following:
>
> - Elements of a sequence diagram
>   > - Lifeline
>   > - Activation bars
>   > - Messages
> - How to draw a sequence diagram
>   > - Identify the use case
>   > - Identify the actors and objects
>   > - Identify the order of actions
>   > - Create the diagram
> - Fragment frame in the sequence diagram

A sequence diagram is a **form of communication diagram that illustrates how differnt actors and objects interact with each other or between themselves.**  
 The diagram represents these interactions as an exchange of messages between various entities and the type of exchange.

Sequence diagram also **demonstrate the sequence of events that occur in a specific use case and the logic behind different operations and functions.**

## Elements of a sequence diagram

Various elements make up a sequence diagram.  
 Let's discuss the essential elements of this diagram that appear most often.

### Lifeline

In sequence diagram, we write all entities horizontally.  
 Each entity has a lifeline that represents its existence, i.e., when the entity is activated or deactivated.  
 We illustrate this **using a dotted line below the entity.**

> We represent different objects, actors, entities, or boundaries in a system using lifelines, and they never overlap each other.
>
> The illustration shows how to visualize a lifeline in UML.  
>  The horizontal boxed are used to denote the objects involved in the interaction.  
>  ![lifeline in a sequence diagram](./images/6-1-lifeline%20of%20sequence%20diagram.pnghttps://www.educative.io/answers/cap-theorem-consistency-availability-and-partition-tolerance)

### Activation bar

Activation bars indicate the **active period** of an object, that is, the time when an object sends or receives messages.  
 We draw them using a simple verticle boxes on the lifeline.

![activation bar in a sequence diagram](./images/6-2-activation%20bar%20of%20a%20sequence%20diagram.png)

### Messages

In sequence diagrams, a message is an interaction between two objects.  
 It can be in the form of sending and receiving messages, invoking an operation, or creating a new object or entity.  
 Messages are drawn horizontally in any direction: left to right, right to left, or back to themselves.

Different types of messages are represented using different arrows.  
 Let's look at the type of messages:

1.  A **synchronous message** is a type of message where the sender has to wait for the receiver to return a response before it can perform another operation.  
    We draw synchronous messages using a solid line with a filled arrowhead.
    ![a synchronous message](./images/6-3-synchronous%20message.pngs)
2.  An **asynchronous message** is a type of message where the sender does not have to wait for a response from the receiver.  
    The sender can continue sending messages to other objects.  
    We can draw the asynchronous message using a solid line with an open arrowhead.
    ![an synchronous message](./images/6-4-asynchronous%20messge.png)
3.  A **synchronous return** is a type of message generated in response to a synchronous call. A synchronous message has to be paired with a synchronous return message.  
    It means that the receiver has processed the message and sent a response.  
    We can draw synchronous return message using a dotted line with a filled arrowhead.
    ![a synchronous return message](./images/6-5-sychronous%20return%20message.png)
4.  A **create message** indicates that a new object is created during an interaction. New objects can be created as a result of some message or operation.  
    We can draw it like this:
    ![a create message](./images/6-6-a%20create%20message.png)
5.  A **destroy message** indicates that an object is destroyed during a sequence of events.  
    Objects can be destroyed as a result of some message or operation, and their lifeline ends.  
    We can draw it like this:
    ![a destroy message](./images/6-7-a%20destroy%20message.png)
6.  A **lost message** is a message that initiates from an object but does not reach its endpoint. It appears as a message that is terminated.  
    A **found message** is a message that is received, but the sender is unknown. It appears as a message that reaches an endpoint but does not initiate from any object.  
    We draw **lost messages as an arrow ending with a circle** and **found messages with an arrow starting with a circle.**  
    ![the lost and found message](./images/6-8-lost%20and%20found%20message.png)

## How to draw a sequence diagram

To create a self-explanatory sequence diagram, there are a number of steps that we need to follow.  
(important to understand that there isn't one correct way of creating a sequence diagram.)

> In this lesson, we introduce a methodology that will help us break down the problem into smaller, achievable tasks.  
>  Let's take a look at the steps.
>
> ### Identify the use case
>
> It is essential to know our use case. The sequence diagram is a means to define the sequential order of events that occur in that use case.
>
> > > Let's build on a simple scenario where a customer wants to withdraw cash from an ATM. Our use case will be as follows:
> > > ![use case for cash withdrawal](./images/6-9-use%20case%20for%20cash%20withdrawal.png)
>
> ### Identify the actors and objects
>
> > > Now list down all the actors and objects that will be involved in the entire sequence. These would be the following:
> > >
> > > - Customer
> > > - ATM
> > > - Transaction
> > > - Account
> > > - Cash dispenser
>
> ### Identify the order of actions
>
> We have identified the entities onvolved in the cash withdrawal sequence, but we don't know how these entities will interact with each other.
>
> > > It is important that we note down the action and the order in which they will occur. Here's how we can define the interaction in steps:
> > >
> > > 1. The customer requests a cash withdrawal from the ATM with their account information and the amount.
> > > 2. The ATM initiates a cash withdrawal transaction against the account and the given amount.
> > > 3. The transaction amount is verified for the given account.
> > > 4. In case the amount entered is valid, the account verifies the transaction.
> > > 5. The ATM signals the cash dispenser to release the required cash amount.
> > > 6. The cash dispenser confirms the release of cash.
> > > 7. The ATM prompts the user to collect the cash.
>
> ### Create the diagram
>
> We have identified all the involved objects and entities in the interaction.  
> We have also listed down the order in which the objects will perform these actions.  
> To finally create the sequence diagram, we need to relate these steps with the type of messages that the objects will exchange with each other.
>
> > > Here's a possible diagram that we can create for the cash withdrawal scenerio:
> > > ![sequence diagram for cash withdrawal](./images/6-10-sequence%20diagram%20for%20cash%20withdrawal.png)

## Fragment frame in the sequence diagram

> Our goal is to keep the sequence diagram as simple as possible without clutter and information overload.  
>  However, sometimes we need to show more complex actions like conditional actions or loop sequences.

Sequence diagrams allow us to represent complex actions/information using the sequence fragment component.  
We can identify the operator of a fragment in the top left corner of the fragment frame.

> Here are a few examples of fragment operators:
>
> **Alternative (alt):** This operator models the if-else condition. It divides the fragment into parts, and either of the parts can take place based ont the guard condition.
>
> **Option (opt):** This operator models the if condition. The fragment will only execute if the guard condition is met. Otherwise, the entire fragment is skipped, and the interaction continues.
>
> **Loop (loop):** This operator represents a repetitive sequence. The fragment will keep repeating until the guard condition is met.
>
> **Reference (ref):** This operator assists in managing larger diagrams. It allows us to reuse parts of another sequence diagram by providing a reference to it.
>
> > > Let's expand the sequence diagram we created to see how we can build on it further using a sequence fragment.
> > >
> > > ![sequence diagram for cash withdrawal with a sequence fragment](./images/6-11-sequence%20diagram%20with%20sequnce%20fragments.png)
>
> In the diagram above, we add the alternatives operator, which divides the sequence into two fragments.  
>  First fragment takes place if the guard condition is met, while in any other case, the second fragment occurs.
>
> > (here the guard condition is that the balance in the account should be greater than or equal to the amount requested by the customer.)

> Next, let's look at the different elements of an activity diagram and how to construct it....
