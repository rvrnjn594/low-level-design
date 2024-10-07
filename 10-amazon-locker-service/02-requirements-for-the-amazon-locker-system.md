# Requirements for the Amazon Locker Service

Learn about all requirements for the Amazon locker service.

> We'll cover the following:
>
> - Requirement collection

In this lesson, we’ll list the requirements of the Amazon Locker service. This is a very crucial step as requirements define the scope of a problem, so getting them right from the interviewer and understanding them well will make the design of the rest of the system smooth and easy.

## Requirement collection

The requirements for the Amazon Locker service are defined below:

1. While ordering the item(s), the customer can choose the nearest location to pick up the order package from the order.
2. One or more items can be contained in one order. An order will be placed in a package before the delivery.
3. There can be different sizes of lockers including extra small, small, medium, large, extra large, and double extra large.
4. The locker is assigned to the customer based on the size of the order package.
5. When the order package is delivered to the locker location specified by the customer, a 6-digit code will be sent to the customer to open the locker.
6. The package will be kept or placed inside the locker for three days only.
7. If the customer does not pick up the package from their locker within three days, the refund process will be initiated and the customer won't be allowed to pick up the package any longer.
8. Only eligible packages can be placed in the locker such that the size of the package must be less than the size of the locker.
9. There can be multiple lockers at every locker location.
10. The Amazon Locker is accessed within a specific time. Every location has its opening and closing time.  
    Therefore, the customer should pick the package during this time period.
11. The item can be refunded to the Amazon Locker if it doesn't match the expectation of the customer or is faulty, and there is a refund policy available for that product.
12. To return an item, the customer needs to choose the nearest locker location.  
    An available locker will be assigned to them based on the size and location.
13. When the customer picks up the order package from the locker, the locker's state is changed to closed, and the customer will no longer be able to open the locker with the given code.

We've identifies our requirements for the problem, and in the next lesson, we will define different use cases for the amazon locker system.
