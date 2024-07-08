# SOLID: Open Closed Principle

Learn about the Open Closed Principle and its implementation in real-world problems.

> We'll cover the following:
>
> - Introduction
> - Example
>   > - Implementing the Open Closed Principle
> - Conclusion

## Introduction

In 1998, Bertrand Meyer defined the Open Closed Principle (OCP) in the following way,  
 **_"A software artifact should be open for extension but closed for modification."_**

This means that **a system should improve easily by adding new code instead of changing the code core.**  
 This way, the core code always retains its unique identity, making it reusable.

> One might think of OCP as inheritance, but remember that inheritance is only one of the OCP techniques.

We use interfaces because it is open for extension and closed for modification.  
 Therefore, OCP is also defined as **polymorphic OCP.**

## Example

> Suppose Alex had a cardboard business that sold boxes to its clients. We design a class for calculating the volume of boxes. It takes the dimensions and calculates the volume of each box and add it up to calculate the total volume of all boxes, as shown below.
> ![volume calculator class](./images/2-1-volume%20calculator%20class.png)
>
> The algorithm for the volume(Cuboid) function is shown in the flowchart below.
> ![volume(Cuboid) function](./images/2-2-volume%20function.png)
>
> As business grew, Alex also started selling cone-shaped boxes. To integrate the calculation of its volume, we need to make a Cone class and update the volume() function. See the updated classes below.
> ![add a cone class and update the volume method](./images/2-3-after%20adding%20cone%20class.png)
>
> The algorithm for the volume(Shape) function is shown in the flowchart below:
> ![volume(Shape) function](./images/2-4-volume%20function.png)
>
> > With only two types of boxes, the class structure looks fine, but what if Alex decides to deal with more types of boxes, eg, a cylinder box?
> >
> > This will add complexity to the volume(Shape).

We will divide the code into segments using OCP to overcome this complexity.

### Implementing the Open Closed Principle

> We will make a parent class, Shape, which is an abstract class and has a volume() funtion, that is extended by its sub-classes, Cuboid, Cylinder, and Cone.
>
> These derived classes have their own volume() functions according to the shape.
>
> Then we have VolumeCalculator class that only performs one task: adding the volume of all the boxes using the sumVolume() function.
> ![class diagram of VolumeCalculator according to OCP](./images/2-5-volumeCalculator%20according%20to%20OCP.png)

## Conclusion

We can conclude the OCP discussions as follows:

- A software system should be easy to extend without the need for modification in the existing system.  
   For the software systems, this goal is achieved by OCP.
- The system must be divided into small components, which are arranged, so that core code is always protected from new code.

> In the next lesson, we will talk about the Liskov Substitution Principle with its detailed explanation....
