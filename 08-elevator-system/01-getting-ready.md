# Getting Ready: Elevator System

Understand the elevator system problem and learn the questions to simplify this problem.

> We'll cover the following:
>
> - Problem definition
> - Expectations from the interviewee
>
> > - Multiple elevators  
> > - Display  
> > - Optimization
>
> - Design approach
> - Design pattern

## Problem definition

> An elevator is an integral part of buildings that have multiple floors. The elevator car could be in different states, either up or down, or could be stopped on some floor.
>
> - Anyone can request an elevator car from any floor using the buttons on the panel.
> - The elevator car's algorithm will the set the priority and take action accordingly, so the wait algorithm will set the priority and take action accordingly, so the wait time is minimum.
> - Inside an elevator, there will be a panel for passengers to select the floor on which they want to go.
> - The elevator car will have a fixed capacity for the number of passenger and a display to show on which floor the elevator car is currently located.

## Expectations from interviewee

Numerous components are present in a typical elevator system, each with a specific constraints and requirements placed on them.

> The following provides an overview of some of the main expectations that the interviewer will want to hear you discuss in more detail during the interview:
>
> > **Multiple elevators**  
> >  You can also ask the interviewer whehther the system should handle multiple elevators or just the sinle one.
> >
> > 1.  Can there be multiple elevator cars in the building?
> > 2.  How could a one-elevator system be different from a multi-elevator system in terms of user wait and running cost?
> >
> > **Display**  
> >  You may want to ask the interviewer about the display of the elevator system:
> >
> > 1. How can passengers see the status of the elevator car and request an elevator car?
> > 2. Would the display be the same inside and outside of the elevator?
> >
> > **Optimization**  
> >  An interviewer would expect you to ask questions about the optimization of the elevatorr system in terms of wait time, maintenance, throughput, etc.
> >
> > 1. What would be an optimized solution to minimize the wait time of the passengers?
> > 2. How are we going to minimize the running cost of the elevator system?

## Design approach

We'll design this elevator system using the bottom-up design approach.

> - Identify and design the smallest components first, like, the button and door.
> - Use these small components to design bigger components, for example, the panel, elevator car, and building.
> - Repeat the steps above until we design the whole system.

## Design pattern

During an interview, it is always a good practice to discuss the design patterns that an elevator system falls under.

> Stating the design patterns gives the interviewer a positive immpression and shows that the interviewee is well-versed in the advanced concepts of object-oriented design.

> Let's explore the requirements of the elevator system in the next lesson.....
