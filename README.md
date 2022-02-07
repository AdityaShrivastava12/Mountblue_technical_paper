# OOPs Concepts

Object Oriented Programming considers everything as an object. This programming paradigm provides various concepts such as **classes**, **objects**, **inheritance**, **polymorphism**, **abstraction**, **encapsulation**, and **methods**.
## Objects
Objects are basic units of object-oriented programming. These are real-world entities like a pen, chair, glass, dog etc. An object has _state_, _behaviour_ , and _identity_.
- **State** : Properties of an object define its state. It is represented by the attributes of an object.
- **Behaviour** : It describes how an object responds to other objects. It is represented by the methods of an object.
- **Identity** : It gives a unique name to an object.

An object is an instance of a class.
## Classes
A class is a user-defined prototype from which various objects are created. It is a collection of objects. All the objects of the same class have same state and behaviour. For example, animal is a class. Dog, cat, horse are its objects. They have the same state and behaviour. They all have four legs. They have same behaviour that they all walk on four limbs. Sets of properties and methods defined in a class are common to all its objects. Let's look at classes from programming languages perspective. A class has the following components :
- **Modifiers** : These are keywords that set the accessibility of a class. There are two types of modifiers - access modifiers and non-access modifiers. There are four types of access modifiers :
 - **Private** : This modifier would be used for attributes, methods and constructors. The block of code would only be accessible within the declared class.
 - **Public** : This is used for classes as well as their attributes, methods and constructors. If a class is public, then it can be accessed by any other class in any package. In case of attributes and other code blocks, they will be accessible for all classes.
 - **Default** :  A default class will only be accessible by the classes in the same package. If no modifier is set, then this is the default. Any attributes, methods or constructors will also be accessible in the same package.
 - **Protected** : Protected attributes, methods or constructors are accessible in the same package and subclasses.

 We also have non-access modifiers :
  - **Static** : A static attribute or method does not require an object. These attributes and methods belong to a class, rather than an object.
  - **Final** : A class defined as a final class cannot be inherited by other classes. In case of attributes and methods, it indicates that they cannot be modified.
  - **Abstract** : We cannot create objects from an abstract class. It has to be subclassed to be accessible. It means, it must be inherited to other classes. For attributes and methods, it indicates that they do not have implementation in the class, but has to implemented in a subclass. Abstract methods does not have a body.
- **Class keyword** : We need to use `class` keyword to declare a class.
- **Class name** : The convention says that every word in a class name should start with a capital letter.
- **Methods** : A class communicates with other classes through methods. Methods act like a function that describes the behaviour of the class.
- **Constructors** : It is a special method that is called when a class is instantiated using `new` keyword. In simple language, a constructor creates an object of a class. A constructor has the same name as class.
- **New keyword** : We can instantiate a class with the help of `new` keyword. It means `new` keyword is used to create an object of a class.

> Example code

  ```Java
  /* Declaring a class */
  public class Car{
    /* Setting attributes and their values */
    String wheels = "4 wheels";
    String engine = "engine";
    String breaks = "breaks";
    String accelerator = "accelerator";

    /* This is a constructor */
    public Car(){
      System.out.println("This car has :\n" + this.wheels + "\n" + this.engine
      + "\n" + this.breaks + "\n" + this.accelerator);
    }

    /* This is a method */
    public String speed(){
      return "I can run upto 50km/hr";
    }

    public static void main(String[] args){
      /* Creating an object. Swift is an instance of car. It has certain attributes and behaviour */
      Car swift = new Car();
      System.out.println(swift.speed());
    }
  }
  ```
## Abstraction
 Data abstraction is a process where implementation details are hidden from the user and only functionality of class is shown to the user. It does not show any details which are not relevant for the user. Let us take a real life example of data abstraction. A car driver knows how to drive a car, how to use its functionality like accelerator pad, brake pad and steering wheel. But he does not know how the break pad works, how the acceletator pad works and so on. He can see the car but not the inner components and how they work. This is data abstraction. Data abstraction is achieved by abstract classes and interfaces. Abstract classes can not create object or abstract methods can not have a body. We can instantiate an object from a derived class.
 >Example code

 ```Java
 /* Declaring an abstract class */
 abstract class Shapes{
   public Shapes(){
     System.out.println("Shapes constructor called");
   }
   abstract void surfacearea();
 }

 /* Child class */
 class Rectangle extends Shapes{
   public Rectangle(){
     System.out.println("Rectangle constructor called");
   }
   public void surfacearea(){
     System.out.println("length x breadth");
   }
 }

 class Main{
   public static void main(String[] args){

     /* The output will show the order of constructor calls. */
     Shapes obj1 = new Rectangle();
     obj1.surfacearea();
   }
 }
 ```

## Encapsulation
 Encapsulation means wrapping up data and codes in a single unit. To achieve encapsulation, we have to declare all the variables of a class as private. This way, these variables will be hidden from other classes. These variables or data will only be accessible through its own class's member functions. We use setter and getter to set and get data in the class.
 >Example code

```Java
public class Details{
 private String name;
 private int passcode;

 public void setName(String name){
   this.name = name;
 }
 public void setPasscode(int code){
   this.passcode = code;
 }
 public String getName(){
   return this.name;
 }
 public int getPasscode(){
   return this.passcode;
 }
}
```
```Java
class Main{
  public static void main(String[] args){
    Details obj = new Details();
    obj.setName("Aditya");
    obj.setPasscode(1234);
    System.out.println(obj.getName() + "\n" + obj.getPasscode());
  }
}

```
## Inheritance
Inheritance is a mechanism in which a class acquires all the properties and behaviour of another class. By this mechanism we can reuse methods and fields of a class. A class which is created from another class and inherits all its properties is called child class. The class from which another class is created is called parent class. We use `extends` keyword for inheritance.
>Example code

```Java
class Members{
  String discount = "10%";
  int no_of_coupons = 5;
}
class PremiumMembers extends Members{
  String extra_premium_discount = "5%";
}
class Main{
  public static void main(String[] args){
    PremiumMembers Aditya = new PremiumMembers();
    System.out.println(Aditya.discount);
    System.out.println(Aditya.extra_premium_discount);
  }
}
```
## Polymorphism
Polymorphism is the ability to perform a single action in different ways. Object-oriented programming languages can differentiate between methods of same name on the basis of their number of arguements or data-type of arguements. This is called overloading. These languages also provides a feature allows a child class to provide a specific implementation of a method that is already provided by its parent class. This is called overriding.

> Example code

```Java
/* This is overriding */
class Athlete{
  void run(){
    System.out.println("I run track");
  }
}
class Sprinter extends Athlete{
  void run(){
    System.out.println("I run 100m");
  }
}
class Crosscountryrunner extends Athlete{
  void run(){
    System.out.println("I run marathon");
  }
}
class Main{
  public static void main(String[] args){
    Athlete Ajay = new Athlete();
    Ajay.run();
    Athlete Aditya = new Sprinter();
    Aditya.run();
    Athlete Shubham = new Crosscountryrunner();
    Shubham.run();
  }
}
```
##### References
- [W3Schools](www.w3schools.com)
- [GeeksforGeeks](www.geeksforgeeks.org)
- [JavaPoint](www.javapoint.com)
- [Tutorialspoint](www.tutorialspoint.com)
