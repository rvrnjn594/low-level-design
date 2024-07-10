# Code of Elevator System

Write object-oriented code to implement the design of the elevator system problem.

> We'll cover the following:
>
> - Elevator system classes
>   > - Enumerations
>   > - Button
>   > - Elevator panel and hall panel
>   > - Display
>   > - Elevator car
>   > - Door and floor
>   > - Elevator system and building
> - Wrapping up

We've discussed different aspects of the elevator system and observed the attributes attached to the problem using various UML diagrams.  
Let's explore the more practicle side of things, where we will work on implementing the elevator system.  
This is usually the last step in an object-oriented design interview process.

## Elevator system classes

We'll provide skeleton code of the classes designed in the class diagram lesson.

> **Note:** For simplicity, we aren't defining getter and setter functions. The reader can assume that all class attributes are private and accessed through their respective public getter methods and modified only through their public methods functions.

#### Enumerations

First of all, we will define all the enumerations required in the elevator system.  
 According to the class diagram, there are three enumerations used in the system i.e., **ElevatorState**, **Direction**, and **DoorState**.

> **Note:** Javascript does not support enumerations, so we will be using the Object.freeze() method as an alternative that freezed an object and prevents further modifications.

    // definition of enumerations used in elevator system
    enum ElevatorState {
        IDLE,
        UP,
        DOWN
    }
    enum Direction {
        UP,
        DOWN
    }
    enum DoorState {
        OPEN,
        CLOSE
    }

#### Button

Contains implementation of a Button class and its subclasses which are HallButton and the ElevatorButton.  
 The Button class has a pure virtual function **isPressed()** in it.

    public abstract class Button {
        private boolean status;
        public pressDown();
        public abstract boolean isPressed();
    }
    public class DoorButton extends Button {
        public boolean isPressed() {
            // Definition
        }
    }
    public class HallButton extends Button  {
        private Direction buttonSign;
        public boolean isPressed() {
            // definition
        }
    }
    public class ElevatorButton extends Button  {
        private int destinationFloorNumber;
        public boolean isPressed() {
            // definition
        }
    }

#### Elevator panel and hall panel

ElevatorPanel and the HallPanel are classes which use the instances of ElevatorButton and HallButton respectively.

    public class ElevatorPanel {
        private List<ElevatorButton> floorButtons;
        private DoorButton openButton;
        private DoorButton closeButton;
    }
    public class HallPanel {
        private HallButton up;
        private HallButton down;
    }

#### Display

Shows implementation of the Display class, responsible fot showing the display inside and outside of the elevator cars.

    public class Display {
        private int floor;
        private int capacity;
        private Direction direction;

        public void showElevatorDisplay();
        public void showHallDisplay();
    }

#### Elevator car

An elevator car contains the instance of Door, Display, and ElevatorPanel.

    public class ElevatorCar {
        private int id;
        private Door door;
        private ElevatorState state;
        private Display display;
        private ElevatorPanel panel;

        public void move();
        public void stop();
        public void openDoor();
        public void closeDoor();
    }

#### Door and floor

Contains code for the Door and Floor classes.  
 In the Door class, the enumeration DoorState is used and the Floor class contains the instances of Display and HallPanel.

    public class Door {
        private DoorState state;
        public boolean isOpen();
    }
    public class Floor {
        private List<Display> display;
        private List<HallPanel> panel;
        public boolean isBottomMost();
        public boolean isTopMost();
    }

#### Elevator system and building

The final class of an elevator system is the **ElevatorSystem** class which will be a Singleton class, which means that the entire system will have only one instance of this class.  
 Moreover, there is a Building class that contains the instances of Floor and ElevatorCar.

    public class ElevatorSystem {
        private Building building;
        public void monitoring();
        public void dispatcher();
        // Private constructor to prevent direct instantiation
        private ElevatorSystem() {
            // Initialize the ElevatorSystem
        }
        // The ElevarSystem is a singleton class that ensures it will have only one active instance at a time
        private static ElevatorSystem system = null;
        // Created a static method to access the singleton instance of ElevatorSytem class
        public static ElevatorSystem getInstance() {
            if (system == null) {
                system = new ElevatorSystem();
            }
            return system;
        }
    }
    public class Building {
        private List<Floor> floor;
        private List<ElevatorCar> elevator;
        private static Building building = null;
        public static Building getInstance() {
            if (building == null) {
                building = new Building();
            }
            return building;
        }
    }

## Wrapping up

We've explored the complete design of an elevator control system in this chapter.  
We've looked at how a basic elevator system can be visualized using various UML diagrams and designed using object-oriented principles and design patterns.
