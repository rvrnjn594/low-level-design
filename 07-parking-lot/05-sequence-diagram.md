# Sequence Diagram for the Parking Lot

Create a sequence diagram for the card payment in the parking lot system and solve a challenge.

> We'll cover the following:
>
> - Card payment

A sequence diagram is a great way to understand the interactions between different entities and objects in the system. There can be different sequence diagrams that we can create for our parking lot system.

For the sake of this lesson, we create sequence diagrams for the following two interactions:

- **Card Payment:** This performs a payment using the card.
- **Sequence challenge:** This is payment verification.

## Card payment

The sequence diagram for the card payment should have the following actors and objects that will interact with each other:

- **Actor:** Customer
- **Object:** CardReader, Payment, and ExitPanel

Here are the steps in the card payment interaction:

1. The customer inserts the card into the card reader.
2. The card reader initiates a payment for the required parking fee.
3. The payment processes the payment and returns the payment status.
4. The card reader ejects the card.
5. If the payment is successful:
   - The customer requests a receipt for the transaction.
   - The exit panel prints a receipt for the customer.
6. If the payment is unsuccessful:
   - The customer sees an error message for an unsuccessful Payment.  
     **Note:** The **Payment** object is created when a vehicle enters the parking lot.

> Based on the order above, the sequence diagram of the card payment in a parking lot system is given below:
> ![sequence diagram for the card payment](./images/5-1-sequence%20diagram%20for%20the%20card%20payment.png)

## Sequence challenge: Payment verification

> The skeleton below represents the payment verification sequence diagram.
>
> Here the payment status of the ticket is currently unpaid and the parking fee has to be calculated.
>
> ![sequence diagram for payment verification](./images/5-2-sequnce%20diagram%20for%20payment%20verification.png)
>
> Notice the arrows are numbered 1 to 6.  
> The correct sequence of the order they should appear in the skeleton of the sequence diagram is:
>
> 1. scanTicket(ParkingTicket)
> 2. checkPaymentStatus(ParkingTicket)
> 3. paymentStatus = unpaid
> 4. calculateParkingFee(ParkingTicket)
> 5. return parkingFee
> 6. requestPayment(parkingFee)

[sequence diagram for payment verification : solution](./images/5-3-sequence%20diagram%20of%20payment%20verification.png)

> In the next lesson, we will create activity diagrams for the parking lot design problem.
