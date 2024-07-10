# Sequence Diagram for the Elevator System

Visualize the sequence diagram for calling the elevator.

> We'll cover the following:
>
> - Elevator call
> - Elevator ride

A sequece diagram is a great **way to understand the interactions between different entities and objects in the system.**

> There can be different sequence diagrams that we can create for our elevator system.
>
> We will create sequence diagram for the following two interactions:
>
> - **Elevator call:** The passenger calls the elevator.
> - **Elavator ride:** The passenger rides the elevator to a floor.

## Elevator call

The sequence diagram for an elevator call should have the following actors and objects that will interact with each other:

- **Actors:** Passenger
- **Objects:** HallButton, ElevatorSystem, Dispatcher, ElevatorCar, and Door

> Here are the steps in the elevator call interactions:
>
> 1. The passenger presses the hall button to call the elevator.
> 2. The hall button signals the elevator system to call an elevator car to the passenger's floor.
> 3. The elevator system informs the dispatcher to select the best car.
> 4. The dispatcher returns the best car to the system.
> 5. The elevator system signals the elevator car to move to the passenger's floor.
> 6. The elevator car signals the system when it arrives on the floor.
> 7. The system signals the hall button that the elevator has arrived.
> 8. The hall button is unpressed.
> 9. The elevator system signals the doors to open.
> 10. The door opens for the passenger.
>
> Based on the order above, the sequence diagram for an elevator call in the elevator system is given below:
>
> ![sequence diagram for an elevator call](./images/5-1-sequence%20diagram%20for%20an%20elevator%20call.png)

## Elevator ride

> Sequence diagram for the elevator ride interaction.
>
> ![sequece diagram for elevator ride](./images/5-2-sequence%20diagram%20for%20elevator%20ride.png)

> Next, let's look at the activity diagrams for the elevator systems to understand **the control flow of the system....**
