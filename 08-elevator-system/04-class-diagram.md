# Class Diagram for the Elevator System

Learn to create a class diagram for the elevator system problem using the bottom-up approach.

> We'll cover the following:
>
> - Components of an elevator system
>   > - Button, Elevator panel and hall panel, Display, Door, Elevator car, Floor, Building, Elevator system, Enumerations
> - Relationship between the classes
>   > - Aggregation, Composition, Inheritance
> - Class diagram of the elevator system
> - Design pattern
> - Additional requirements
>   > - FCFS, SSTF, SCAN, LOOK

In this lesson, design the classes, abstract classes, and interfaces based on the requirements that we have previously gathered from the interviewer in our elevator system.

## Components of an elevator system

As mentioned earlier, we should design the elevator system using a bottom-up approach.

> Therefore, we will first identify and design classes of the smaller components like button, door, and floor.  
>  Then, we will create the class of the entire elevator control system, which will contain these smaller components.

#### Button

> - **Button is an abstract class.** There can be two types of buttons i.e., the elevator button and the hall button.  
>   Status of the button determines whether the button is pressed or unpressed.  
>    We can press the button or check the status of the button through the Button class.
>
> The **ElevatorButton** subclass is inherited from the Button class and represents the buttons that are inside the elevator.
>
> Similar to the **ElevatorButton**, **HallButton** is also subclass of the Button class. This class represents the buttons that are outside the elevator.
>
> > This class used the enumeration Direction to specify whether the button is for going up or down.  
> > The hall button has two important pieces of information,
> >
> > - the floor from where the button is pressed and
> > - the direction in which the passenger wants to move.
> >
> > UML representation of these classes is shown below:
> > ![class diagram of Button and its derived classes](./images/4-1-class%20diagram%20of%20Button%20and%20its%20derived%20classes.png)

#### Elevator panel and hall panel

> **ElevatorPanel** is a class which is used to represent the complete grid of buttons inside the elevator.
>
> > In the elevator panel, we will have a list of buttons for selecting the destination floor of the elevator and two buttons for closing and opening the elevator.
>
> While the **HallPanel** class represents the buttons that are outside the elevators.
>
> > The hall panel consists of only two buttons: up and down.
>
> Both the elevator panel and the hall panel are used to take input from the passenger.  
> ![class diagram of HallPanel and ElevatorPanel classes](./images/4-2-class%20diagram%20of%20hall%20panel%20and%20elevator%20panel.png)

#### Display

> Every elevator has a display to represent the current floor number and direction (up or down) of an elevator. It also gives information about the capacity of the elevator.
>
> The **Display** class consists of floor number, capacity, and direction.
>
> > It has seperate methods for both the elevator display and hall display.
> > ![class diagram of the Display class](./images/4-3-class%20diagram%20of%20Display%20class.png)  
> > The **showHallDisplay()** will present only the current floor the lift is in and direction of the lift while the **showElevatorDisplay()** will display all of the class attributes.

#### Door

> **The Door class symbolizes the door of an elevator.**
>
> > This class had a reference to enum **DoorState** which depicts that the status of the door can be either open or closed.
> >
> > ![class diagram of the Door class](./images/4-4-class%20diagram%20of%20Door%20class.png)

#### Elevator car

> **ElevatorCar** is the class that expresses the elevators of the building.
>
> > Each elevator has a unique ID. This class consits of an enumeration named **state** that tells the present state of the elevator.  
> >  Moreover, in every elevator car, there is a door, an elevator panel, and a display.  
> >  The elevator car can start moving or stop on any floor.  
> > ![class diagram of the Elevator class](./images/4-5-class%20diagram%20of%20ElevatorCar%20class.png)

#### Floor

> The **Floor** class represents the floors of a building.
>
> > Each floor consists of a number/list of hall panels to call the lift and has displays to indicate the current floor and direction of the lift since there is a seperate panel and display for each elevator.
> >
> > ![class diagram of the Floor class](./images/4-6-class%20diagram%20of%20Floor%20class.png)

#### Building

> The building class represents an actual building that consits of the number of floors and elevators.  
> ![class diagram of the Building class](./images/4-7-class%20diagram%20of%20Building%20class.png)

#### Elevator system

> **ElevatorSystem** is the main functional class of the whole elevator control system.
>
> > The elevator system has a display of each elevator and monitors the elevator cars.  
> > The elevator system has a dispatcher to select the best elevator car.  
> > Moreover, the system takes control of the elevators doors.  
> > ![class diagram of the ElevatorSystem class](./images/4-8-class%20diagram%20of%20ElevatorSystem%20class.png)

#### Enumerations

> Enumeration is generally a data type in which only a specific set of constants can be stored.
>
> - **ElevatorState:** describes the state of an elevator, which could be idle, up, or down.
> - **Direction:** when the elevator is not an idle state, it describes the direction of the motion of an elevator which could be up or down.
> - **DoorState:** when the elevator is in an idle state, it describes the statud of a door of an elevator that could be open or close.
>
> ![enums in the elevator system](./images/4-9-enums%20in%20elevator%20system.png)

## Relationship between the classes

#### Aggregation

> **ElevatorSystem** has an aggregation relationship with **Building**.  
> ![association relationship between classes](./images/4-10-association%20relationship%20between%20classes.png)

#### Composition

> - Building is composed of ElevatorCar and Floor.
> - ElevatorCar is composed of Door, ElevatorPanel, and Display.
> - Floor is composed of HallPanel and Display.
> - HallPanel is composed of the HallButton.
> - ElevatorPanel is composed of the ElevatorButton.
>
> ![composition relationship between classes](./images/4-11-composition%20relationships%20between%20classes.png)

#### Inheritance

> - Both ElevatorButton and HallButton extend the Button class.

## Class diagram of the elevator system

> Here is complete diagram for our elevator system.
>
> ![class diagram of elevator system](./images/4-12-class%20diagram%20of%20elevator%20system.png)

## Design pattern

- The **Strategy** design pattern can be applied here **since the system could have multiple dispatch request strategy classes.**  
   Therefore, depending on the particular layout of the building and its scenerios, we choose a set of dispatch request strategy classes.
- We can also use the **State and Delegation design pattern** for this problem.  
   Instead of implementing all methods on its own, the context object stores a reference to one of the state objects that represents its current state and delegates all the state-specific tasks to that object.
  > For example, elevators have multiple states like working or idle, etc.  
  >  Based on the state, the system infers which method or behavior of the elevator should be invoked.

## Additional requirements

The additional requirements can be about how the dispatcher works in the elevator system.

The interviewer can ask to devise an algorithm to optimize any of these:

- To minimize the wait time of the system.
- To minimize the wait time of the passenger.
- To maximize throughput.
- To minimize the power usage or cost.

> To optimize the elevator system, we have different dispatching algorithms.  
>  FCFS, SSTF, SCAN and LOOK.
>
> ---
>
> #### FCFS (First Come First Serve)
>
> Advantage: It is simple and easy to implement.  
> Drawback: Extra elevator movements occur by this algorithm which results in more power usage and cost.
>
> > To implement FCFS, we can use a queue data structures to keep track of which passenger comes first

FCFS is a scheduling algorithm by which the passenger who comes first gets the elevator car and reaches the destination.

There are four states of an elevator car with respect to the passenger:

- The elevator car is in an idle state.
- The elevator car is moving towards the passenger and in the same direction the passenger wants to go.
- An elevator car is moving towards the passenger but in the opposite direction the passenger wants to go.
- The elevator car is moving away from the passenger.

In this algorithm, the dispatcher will try to find elevators that are in either of the first two states and ignore those elevators which are in either of the last two states.

> #### SSTF (Shortest Seek Time First)
>
> SSTF is an algorithm in which the passenger who is closest to the elevator car would get the elevator car.
>
> > This is considered better than FCFS since less elevator movement is required as compared to the FCFS since less elevator movement is required as compared to the FCFS algorithm.
> >
> > This algorith also results in increased throughput.  
> >  However, there is a loophole in this method where it always chooses the minimum distant passengers and ignore the farther ones completely.
>
> To implement this algorithm, we can use a priority queue, min-heap, or an array data structure.
>
> #### SCAN (Also known as the Elevator algorithm)
>
> The elevator car starts from one end of the building and moves towards the other end, servicing requests in between.
>
> > Advantage: It serves multiple requests in parallel.  
> >  However, it results in increased cost as the elevator car only changes its direction at either the top floor, or the lowest floor.
>
> The implementation of SCAN can be done using two boolean arrays or a single HashMap, or two priority queues data structures to track the floor where the elevator should stop.
>
> #### LOOK (Also known as look-ahead SCAN algorithm)
>
> It is an improved version of SCAN Algortihm.
>
> > In this algorithm, the elevator car stops when there is no request in front of them. It will move again on the basis of the request.
>
> Advantage: Elevator car does not always go till the end of the building but can change its direction in between.
>
> The algorithm can be implemented using a HashMap, TreeMap, or binary search tree data structure.
>
> ---

> Completed the class diagram according to the requirements.  
>  Let's design the sequence diagram of the elevator control system in the next lesson.....
