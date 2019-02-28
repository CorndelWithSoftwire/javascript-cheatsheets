# Object Oriented Programming

Java is an object-oriented programming (OOP) language, which means that we design classes, objects and methods that hold certain data and can perform certain actions. This is important in the construction of larger and more complex Java programs.

## Classes

The fundamental concept in object-oriented programming is the _class_. A _class_ is a description of a set of data, and instructions for how that data should behave.

Java has a lot of pre-defined classes to use (`String` is one example of a class) but we can also define our own custom classes.

### Defining a class

A class in Java is defined using the following syntax:

```java
public class Car {

}
```

This creates a class named `Car` - although it doesn't contain any data or behaviour yet!

### Instance variables

When creating a new class, there will be specific pieces of data that you want that class to hold. These are known as _instance variables_.

For instance, given a car, we might want to know how many doors it has and what colour it is. This can be done by defining instance variables like this:

```java
public class Car {

    private int numberOfDoors;
    private String colour;

}
```

### Constructors

Now that we've decided what data the `Car` class should contain, we need a way to actually create a `Car` and put some real data into it. In Java, this is done using a _constructor_.

A constructor is a special method on a class which contains a set of instructions for how to initialise a new instance of the class. Constructors take inputs which can be used as part of the initialisation.

Here's an example constructor for a `Car` which takes a number of doors and a colour as inputs, and sets the instance variables on `Car` to be equal to those given inputs:

```java
public class Car {

    private int numberOfDoors;
    private String colour;

    public Car(int numberofDoors, String colour) {
        this.numberOfDoors = numberOfDoors;
        this.colour = colour;
    }
}
```

In Java, the name of the constructor must always be exactly equal to the name of the class - in this case, `Car`.

### Instances

We now have a definition for what a `Car` should look like, and instructions for how to create a new one. We are now able to actually create an _instance_ of the `Car` class as follows:

```java
Car myCar = new Car(5, "silver");
```

This creates a variable (called `myCar`) which is of type `Car`. The `new` keyword is used to tell Java that we want a new `Car` and that we should use the constructor of the `Car` class to create it. Here, the inputs to our constructor were `5` and `"silver"`. This would construct a car with 5 doors and which is silver-coloured.

## Methods

So far we've decided what sort of data should be on the `Car` class, and worked out how to create _instances_ of `Car`.

But classes do not only contain data - they also contain _methods_. A method is a pre-defined set of instructions that will be carried ot when you _call_ the method.

We can add some methods to our `Car` class like this:

```java
public class Car {

    private int numberOfDoors;
    private String colour;

    public Car(int numberofDoors, String colour) {
        this.numberOfDoors = numberOfDoors;
        this.colour = colour;
    }

    public void startEngine() {
        System.out.println("Vrooom!");
    }

    public int getNumberOfDoors() {
        return this.numberOfDoors;
    }

    public void paint(String colour) {
        this.colour = colour;
    }
}
```

A method definition consists of several parts:

1. An access modifier (usually `public` or `private`)
2. The type of object that the method returns
3. A name for the method
4. A list of inputs that the method needs, in parentheses
5. A block of code that will be executed when the method is _called_

The three methods we added to the `Car` class are broken down into their parts like this:

### `startEngine`

1. Access modifier `public`
2. Returns nothing (this is known as `void` in Java)
3. Called `startEngine`
4. Takes no inputs
5. Prints "Vrooom!" to the console when called

### `getNumberOfDoors`

1. Access modifier `public`
2. Returns an `int`
3. Called `getNumberOfDoors`
4. Takes no inputs
5. Returns the number of doors the car has when called

### `paint`

1. Access modifier `public`
2. Returns nothing (`void`)
3. Called `paint`
4. Takes a single `String` input, called `colour`
5. Sets the colour of the car to be the input colour when called

