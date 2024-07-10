# Getting Ready: Parking Lot

Let's make an object-oriented design for a **multi-entrance and exit parking lot system.**

> We'll cover the following:
>
> - Problem definition
> - Expectations from the interviewee
>   > - Payment flexibility
>   > - Parking spot type
>   > - Vehicle types
>   > - Pricing
> - Design approach
> - Design pattern

## Problem definition

> A parking lot is a designated area for parking vehicles and is a feature found in almost all popular venues such as shopping malls, sports stadiums, offices, etc.
>
> In a parking lot, there are a fixed number of parking spots available for different types of vehicles.  
>  Each of these spots is charged according to the time the vehicle has been parked in the parking lot.
>
> The parking time is tracked with a parking ticket issued to the vehicle at the entrance of the parking lot.
>
> Once the vehicle is ready to exit, it can either pay at the automated exit panel or to the parking agent at the exit using a card or cash payment method.
> ![layout of the parking lot](./images/Screenshot%202024-07-09%20at%205.06.52 AM.png)

## Expectations from the interviewee

In a typical parking lot system, there are several components each with specific constraints and requirements.

Following section provides an overview of some major expectations the interviewer will want an interviewee to discuss in more detail during the interview:

- **Payment flexibility**  
   One of the most significant attributes of the parking lot system is the payment structure that it provides to its customer.  
   An interviewer would expect you to ask questions like these:
  - How are customers able to pay different exit points (i.e., either at the automated exit panel or to the parking agent) and by different methods (cash, credit, coupon)?
  - If there are multiple floors in the parking lot, how will the system keep track of the customer having already paid on a particular floor rather than at the exit?
- **Parking spot type**  
   Another topic of discussion that an interviewer would expect you to be aware of is the different parking spot types - _handicapped, compact, large, and motorcycle_ - regardless which you can ask the following questions:
  - How will the parking capacity of each lot be considered?
  - What happens when a lot becomes full?
  - How can one keep track of the free parking spots on each floor if there are multiple floors in the parking lot?
  - How will the division of the parking spots be carried out among the four different parking spot types in the lot?
- **Vehicle types**  
   Similar to the parking spot, an interviewer would also expect you to discuss the different vehicle types - _car, truck, van, motorcycle_ - which can have the following set of questions:
  - How will capacity be allocated for different vehicel types?
  - If the parking spot of any vehicle type is booked, can a vehicle of another type park in the designated spot?
- **Pricing**  
   We touched upon the payment structure offered by the parking lot system.  
   Now, the pricing model needs to be clarified from the interviewer, and therefore you may ask questions like these:
  - How will pricing be handled? Should we accomodate having different rated for each hour? For example, customers will have to pay 4$ for the first hour, 3.5$ for the second and third hours, and 2.5$ for all the subsequent hours.
  - Will the pricing be the same for the different vehicle types?

## Design approach

We are going to design this parking lot system using the bottom-up design approach.  
For this purpose, we will follow the steps below:

- Identify and design the smallest components first, like, the vehicle and the parking spot types.
- Use these small components to design bigger components, for example, the payment system at the exit.
- Repeat the steps above until we design the whole system like the parking lot.

## Design pattern

During an interview, it is always a good practice to discuss the design patterns that a parking lot system falls under.

> Stating the design patterns gives the interviewer a positive impression and shows that the interviewee is well-versed in the advanced concepts of object-oriented design.

Question to think about -

> "Which design pattern(s) should be used for solving the problem of managing a parking lot efficiently? Explain your choices(s)."
>
> **Hint:** Think about a design pattern that ensures there is only one instance of the parking lot system.  
>  Also, consider a pattern that could help in creating different types of parking spots or handling differnt payment methods.

> Let's explore the requirements of the parking lot system in the next lesson....
