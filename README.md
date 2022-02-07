# OOPs Concepts

Object Oriented Programming considers everything as an object. This programming paradigm provides various concepts such as **classes**, **objects**, **inheritance**, **polymorphism**, **abstraction**, **encapsulation** and **methods**.
## Objects
Objects are basic units of object-oriented programming. These are real world entities like pen, chair, glass, dog etc. An object has _state_, _behaviour_ and _identity_.
- State : Properties of an object define its state. It is represented by attributes of an object.
- Behaviour : It describes how an object responds to other objects. It is represented by methods of an object.
- Identity: It gives an unique name to an object.

An object is an instance of a class.
## Classes
A class is a user defined prototype from which various objects are created. It is a collection of objects. All the objects of the same class have same state and behaviour. For example, animal is a class. Dog, cat, horse are its objects. They have same state and behaviour. They all have four legs. They have same behaviour that they all walk on four limbs. Sets of properties and methods defined in a class are common to all its objects. Let's look at classes from programming languages perspective. A class has following components :
- Modifiers : These are keywords that sets accessibility of a class. There are two types of modifiers - access modifiers and non-access modifiers. There are four types of access modifiers :
 - Private : This modifier would be used for attributes, methods and constructors. The block of code would only be accessible within the declared class.
 - Public : This is used for classes as well as their attributes, methods and constructors. If a class is public, then it can be accessed by any other class in any package. In case of attributes and other code blocks, they will be accessible for all classes.
 - Default :  A default class will only be accessible by classes in the same package. If no modifier is set, then this is the default. Any attributes, methods or constructors will also be accessible in the same package.
 - Protected : protected attributes, methods or constructors are accessible in the same package and subclasses.

 We also have non-access modifiers :
  - Static : A static attribute or method does not require an object. These attributes and methods belongs to a class, rather than an object.
  - Final : A class defined as a final class cannot be inherited by other classes. In case of attributes and methods, it indicates that they cannot be modified.
  - abstract : We cannot create objects from an abstract class. It has to be subclassed to be accessible. It means, it must be inherited from other class. For attributes and methods, it indicates that they do not have implementation in the class, but has to implemented in a subclass. Abstract methods doesnt have a body.
- Class keyword : We need to use `Class` keyword to declare a class.
- Class name : The convention says that every word in a class name should start with a capital letter.
- Methods : A class communicates with other classes through methods. Methods act like a function which describes behaviour of the class.
- New keyword : We can intantiate a class with the help of `new` keyword.

## Abstraction
 Data abstraction is a process where implementation details are hidden from the user and only functionality of class is shown to the user. It does not show any details which are not relevant for the user. Let us take a real life example of data abstraction. A car driver knows how to drive a car, how to use its functionality like accelerator pad, brake pad and steering wheel. But he does not know how the break pad works, how the acceletator pad works and so on. He can see the car but not the inner components and how they work. This is data abstraction.

## Encapsulation
 Encapsulation means wrapping up data and codes in a single unit. To achieve encapsulation, we have to declare all the variables of a class as private. This way, these variables will be hidden from other classes. These variables or data will only be accessible through its own class's member functions. We use setter and getter to set and get data respectively in the class.

## Inheritance
Inheritance is a mechanism in which a class acquires all the properties and behaviour of another class. By this mechanism we can reuse methods and fields of a class. A class which is created from another class and inherits all its properties is called child class. The class from which another class is created is called parent class.

## Polymorphism
Polymorphism is the ability to perform a single action in different ways. Object-oriented programming languages can differentiate between methods of same name on the basis of their number of arguements or data-type of arguements. This is called overloading. These languages also provides a feature allows a child class to provide a specific implementation of a method that is already provided by its parent class. This is called overriding.
