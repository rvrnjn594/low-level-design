# Use Case Diagram for the Elevator System

Learn how to define use cases and create the corresponding use case diagram for the elevator system.

> We'll cover the following:
>
> - System
> - Actors
>   > - Primary actors
>   > - Secondary actors
> - Use Cases
>   > - Passenger
>   > - System
> - Relationships
>   > - Generalization
>   > - Associations
>   > - Include
> - Use case diagram

> Let's build the use case diagram of the elevator system and understand the relationship between its different components.

First, we will define the different elements of our elevator, followed by the complete use case diagram of the system.

## System

Our system is an **"elevator."**

## Actors

Define our elevator system's main actors.

#### Primary actors

- **Passenger:**  
   This actor is the passenger in an elevator.
  > It can request an elevator, open and close the door of an elevator, move up and down using the elevator, and press the emergency button.

#### Secondary actors

- **System:**  
   It can open and close the elevator door, display floor level and move the elevator according to the dispatcher algorithm.

## Use Cases

(define use cases for the elevator)  
Listed the use cases according to their respective interactions with a particular actor.  
(Note: use cases can occur multiple times because they are shared among different actors in the system.)

#### Passenger

- **Press elevator panel button:**  
   To press the button on the elevator panel to select the destination floor, request to open/close the elevator door while it is stopped, or call an emergency.
- **Press hall panel button:**  
   To press the button on the hall panel to select the request for the elevator.

### System

- **Move/stop elevator:** To move up or down or to stop the elevator on a specific floor.
- **Dispatcher algorithm:** For proper elevator functionality according to the algorithm.
- **Display (inside/outside):** To display the floor number on the screen inside and outside the elevator.
- **Open/close door:** To open and close the elevator door.

> There are some use cases that are not directly related to any actor.
>
> - **Request for elevator:** To request the elevator.
> - **Floor request:** To submit a request for the destination floor.
> - **Door open/close request:** To submit a request to open/close the elevator door.
> - **Call Emergency:** To call the support team in case of emergency.

## Relationships

Relationships betweem and among actors and their use cases:

#### Generalization

**"Press elevator panel button"** use case has a generalization relationship with "Floor request", "Door open/close request", and "Call emergency" use cases.

#### Associations

Association relationship between actors and their use cases.

- **Passenger:** Press elevator panel button and Press hall panel button.
- **System:** Dispatcher algorithm, Open/close door, Display(inside/outside), Move/stop elevator.

#### Include

- **"Floor request"** use case has an include relationship with the "Move/stop elevator" use case.
- **"Door open/close request"** use case has an include relationship with the "Open/close door" use case.
- **"Press hall panel button"** use case has an include relationship with the "Request for elevator" use case.

## Use case diagram

![use case diagram of elevator system](./images/3-1-use%20case%20diagram%20of%20elevator%20system.png)

> In the next lesson, we will discuss the class diagram with a detailed explanation of all classes and their relationship.
