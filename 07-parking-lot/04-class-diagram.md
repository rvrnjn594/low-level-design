# Class Diagram for the Parking Lot

Learn to create a class diagram for the parking lot system using the bottom-up approach.

> We'll cover the following:
>
> - Components of a parking system
> - Relationship between classes
> - Class diagram of the parking lot system
> - Design pattern
> - Additonal requirements

We will identify and design classes, abstract classes, and interfaces based on the requirements we have previously gathered from the interviewer in our parking lot system.

## Components of a parking lot system

As mentioned earlier, we should design the parking lot system using a bottom-up approach. Therefore, we will first identify and design the classes of the smaller components like vehicles and parking spots.  
 Then, we will create classes of the entire parking lot system, including these smaller components.

> #### Vehicle
>
> Our parking system should have vehicle object according to the requirements.  
>  There are two ways to represent a vehicle in our system:
>
> - Enumeration
> - Abstract class
>
> ###### Enumeration vs. abstract class
>
> **The enumeration class creates a user-defined data type that has the four vehicle types as values.**
>
> This approach is not proficient for OOD because if we want to add one more vehicle type later, then we would need to update the code in multiple places in our code, and this would violate the Open Closed principle states that classes can be extended but not modified.  
>  Therefore, it is not recommended to use enumeration data type as it is not a scalable approach.  
>  (Later, we will use the PaymentStatus enum in our parking lot design as it won't require further modifications.)
> ![class diagram of Vehicle and its derived classes](./images/4-1-class%20diagram%20of%20Vehicle%20and%20its%20derived%20classes.png)
>
> #### Parking spot
>
> Similar to the Vehicle class, the ParkingSpot should also be an abstract class.  
>  These classes can be derived from the parking spot abstract class.  
> ![class diagram of the ParkingSpot and its derived classes](./images/4-2-class%20diagram%20of%20ParkingSpot%20and%20its%20derived%20classes.png)
>
> #### Account
>
> Similar to Vehicle and ParkingSpot classes, Account should also be an abstract class.  
>  There are two child classes: Admin and ParkingAgent. These classes can be derived from the account abstract class.
> ![class diagram of Account and its derived classes](./images/4-3-class%20diagram%20of%20Account%20and%20its%20derived%20classes.png)
>
> #### Display board
>
> This class represents the free parking spot types and the number of empty slots.  
> ![class diagram of the DisplayBoard class](./images/4-4-class%20diagram%20of%20the%20DisplayBoard%20class.png)
>
> #### Entrance and exit
>
> The Entrance class is responsible for generating the parking ticket whenever a vehicle arrives.  
>  It contains the ID attribute, since there are multiple entrances to the parking lot. It also has the _getTicket()_ method.
>
> The Exit class is resposible for validating the parking ticket's payment before allowing the vehicle to exit the parking lot.  
>  It contains the ID attribute, since there are multiple exits to the parking lot. It also has _validateTicket()_ method.
>
> ![class diagram of the Entrance and Exit classes](./images/4-5-class%20diagram%20of%20entrance%20and%20exit.png)
>
> #### Parking ticket
>
> The ParkingTicket class is one of the central classes of the system. It keeps track of the entrance and exit times of the vehicles, the amount, and the payment status.
> ![class diagram of the ParkingTicket](./images/4-6-class%20diagram%20of%20parking%20ticket.png)
>
> #### Parking lot
>
> This parking lot system is composed of smaller objects we have already designed.
> ![class diagram for the ParkingLot class](./images/4-7-class%20diagram%20of%20ParkingLot.png)
>
> #### The enumerations and custom data types
>
> The following provides an overview of the enumerations and custom data types used in this problem:
>
> - **PaymentStatus:**  
>    Create an enumeration to keep track of the payment status of the parking ticket, whether it is paid, unpaid, canceled, refunded, and so on.
> - **AccountStatus:**  
>    Create an enumeration to keep track of the status of the account, whether it is active, canceled, closed, and so on.
>   ![Enums in the parking lot system](./images/Screenshot%202024-07-09%20at%208.37.37 AM.png)
>
> ##### Address
>
> We also need to create a custom data type, Address, that will store the location of the parking lot.
> ![Address custom datatype](./images/4-9-Address%20custom%20datatype.png)
>
> ##### Person
>
> The Person class is used to store information related to a person like a name, street address, country, etc.
> ![Person class custom datatype](./images/4-10-person%20class%20custom%20datatype.png)

## Relationship between classes

Now, we'll discuss the relationships between classes we have defined above in our parking lot system.

> #### Association
>
> The class diagram has the following association relationships:
>
> - The **ParkingSpot** has a one-way association with **Vehicle**.
> - The **Vehicle** has a one-way association with the **ParkingTicket**.
> - The **Payment** has a two-way association with **ParkingTicket**.
>   ![association relationship between classes](./images/4-11-association%20relationship%20between%20classes.png)
>
> #### Composition
>
> The class diagram has the following composition relationships:
>
> - The **ParkingLot** class includes **Entrance, Exit, ParkingRate, DisplayBoard, ParkingTicket, and ParkingSpot**.
> - The **ParkingTicket** class includes **Payment** object.
>   ![composition relationship between classes](./images/4-12-composition%20relationship%20between%20classes.png)
>
> #### Inheritance
>
> The following classes show an inheritance relationship:
>
> - The **Vehicle** class includes Car, Truck, Van, and MotorCycle.
> - The **ParkingSpot** class includes handicapped, compacy, large, and motorcycle subclasses.
> - The **Payment** class includes the Cash and CreditCard subclasses.

## Class diagram of the parking lot system

Here is complete class diagram for our parking lot system:
![class diagram of parking lot system](./images/4-13-complete%20class%20diagram%20of%20parking%20lot%20system.png)

## Design pattern

The system itself will have a ParkingLot class.  
 It will use the Singleton design pattern, because there will be only a single instance of the parking lot system.

This parking lot system is also composed of smaller objects that we have already designed, like entrance, exit, parking spots, parking rates, etc.  
 Therefore, it will be a good practice to use the Abstract Factory and Factory design pattern to instantiate all those objects.

## Additional requirements

The interviewer can introduce some additional requirements in the parking lot system, or they can ask some follow-up questions.  
 Let's see examples of additional requirements:

- **Parking floor:**  
  The parking lot should have multiple floors where customers can park their cars. The class diagram provided below shows the relationship of ParkingFloor with other classes:  
  ![realationship of the ParkingFloor class with other classes](./images/4-14-relationship%20of%20ParkingFloor%20class%20with%20other%20classes.png)
- **Electric:**  
   The parking lot should have some parking spots specified for electric cars. These spots should have an electric panel through which customers can pay and charge their vehicles.  
   The class diagram below shows relationship of Electric and ElectricPanel with other classes:  
   ![relationship of Electric and ElectricPanel class with other classes](./images/4-15-relationship%20of%20the%20Electric%20and%20ElectricPanel%20class%20with%20other%20classes.png)

> We have completed the class diagram of the parking lot system according to the requirements.  
>  Now, let's design the sequence diagram of the parking lot system in the next lesson....

---

Let's say that the interviewer asks you that **the parking lot should assign a parking spot closest to the entrance.** How would you go about solving this requirement?

> This requirement is more about how you implement this perking assignment strategy rather than designing it.  
>  The interviewer is really looking at your data structures and algorithms skilld in this requirement.

In this scenerio, let's say we have four entrances and would like to return to the parking spot which is nearest to the entrance from where the customer is entering the parking lot.  
 **The best approach is to implement it using a min-heap**.

- We will declare four min-heaps. We will add all parking spots to these min-heaps, so there will be a min-heap for each entrance. These min-heap will store the parking spots in the order of the shortest distance from the entrance.
- We will also declare the following two sets of parking spots:
  - A set of available parking spots.
  - A set of reserved parking spots.
- We have a map of min-heaps where the key is the entrance ID, and the value is a min-heap. When the user calls the _getParkingSpot_ method, we get the entrance ID which gives us the min-heap for that entrance and allows us to pop the top element to get the parking spot.
- We mark the parking spot as reserved and remove it from the available set. We also remove it from the min-heap of other entrances.

---
