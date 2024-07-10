# Activity Diagram for the Parking Lot

Create some activity diagrams for the parking lot problem.

> We'll cover the following:
>
> - Vehicle entering the parking lot
>   > - States
>   > - Actions
> - Activity challenge: The customer pays the parking ticket

An activity diagram is a great way **to visualize the flow of messages from one activity to the other in the system.**

> There can be different activity diagrams that we can create for our parking lot system.  
>  For this lesson, we will create activity diagram for the following two activities:
>
> - The vehicle entering the parking lot.
> - **Activity challenge:** Customer pays the parking ticket.

## Vehicle entering the parking lot

The following are the states and the actions that will be involved in this activity diagram.

> #### States
>
> **Initial state:** The customer enters the parking lot.
>
> **Final state:** There are two final states present in this activity diagram, shown below:
>
> - The customer receives the parking ticket through the system.
> - There is no parking slot vacant, so the customer is denied access to the parking lot.
>
> #### Actions
>
> The customer arrives at the parking lot entrance and selects their vehicle type. They are assigned their dedicated parking spot according to their selected vehicle type.  
>  The parking lot then informs us about the availability of that parking spot and allows access accordingly.
>
> Based on the order above, the activity diagram of a vehicle entering a parking lot is given below:
>
> ![activity diagram for the vehicle entering a parking lot](./images/6-1-activity%20diagram%20for%20the%20vehicle%20entering%20a%20parking%20lot.png)
>
> **NOTE:** Here we assume that only a car can be parked in the handicap spot. Access is only available if the car has a disabled person card present.

## Activity challenge: The customer pays the parking ticket

You will help us create an activity diagram of a customer paying a parking ticket at the exit panel.

> The skeleton of the activity diagram below represents that the customer has a valid parking ticket available.
> ![activity diagram for the vehicle entering a parking lot](./images/6-2-activity%20diagram%20for%20customer%20entering%20a%20parking%20lot.png)

---

> We've looked at some of the activity diagrams of our parking lot system. In the next lesson, we will present the code for our designed classes in some of the most popular languages....
