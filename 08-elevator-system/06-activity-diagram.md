# Activity Diagram for the Elevator System

Create some activity diagrams for the elevator system problem.

> We'll cover the following:
>
> - The passenger arrives at the desired floor
>   > - States
>   > - Actions
> - The passenger calls for the elevator

An activity diagram is a great way to visulize the flow of the messages from one activity to the other in the system.

> There can be different activity diagrams that we can create for our elevator system.
>
> In this lesson, we will create activity diagrams for the following two activities:
>
> - The passenger arrives at the desired floor.
> - The passenger calls for the elevator.

## The passenger arrives at the desired floor

> The following are the states and actions that will be involved in this activity diagram.
>
> #### States
>
> **Initial state:** The passenger enters the elevator car.
>
> **Final state:** There are two final states present in this activity diagram.
>
> - The passenger arrives at the destination floor.
> - The passenger is not allowed due to max load/capacity issues.
>
> #### Actions
>
> The passenger enters the elevator car.  
> The elevator car checks if the safety limits are met.  
> The elevator car stops at other passenger's floors.  
> Finally, the elevator car reaches the passenger's desired floor.
>
> Based on the order above, the activity diagram of a passenger arriving at their desired floor is given below.
>
> NOTE: Here, the passenger is just entering the elevator, so either the up or the down button can be pressed.
>
> ![activity diagram for a passenger arriving at their desired floor](./images/6-1-activity%20diagram%20for%20a%20passenger%20arriving%20at%20their%20desired%20floor.png)

## The passenger calls for the elevator

> Activity diagram for the passenger call for the elevator
>
> ![activity diagram for the passenger call for the elevator](./images/6-2-activity%20diagram%20for%20passenger%20calls%20for%20the%20elevator.png)

> In the next lesson, we will present the code for our designed classes.....
