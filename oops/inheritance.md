# Inheritance in Java


Inheritance is an important pillar of OOP(Object Oriented Programming). It is the mechanism in java by which one class is allow to inherit the features(fields and methods) of another class.  

**Important terminology:** 

-   **Super Class:** The class whose features are inherited is known as super class(or a base class or a parent class).
-   **Sub Class:**  The class that inherits the other class is known as sub class(or a derived class, extended class, or child class). The subclass can add its own fields and methods in addition to the superclass fields and methods.
-   **Reusability:** Inheritance supports the concept of “reusability”, i.e. when we want to create a new class and there is already a class that includes some of the code that we want, we can derive our new class from the existing class. By doing this, we are reusing the fields and methods of the existing class.

## How to use inheritance in Java

The keyword used for inheritance is  **extends**.  
Syntax :

```java
class derived-class extends base-class  
{  
   //methods and fields  
}
```  

**Example:** In below example of inheritance, class Bicycle is a base class, class MountainBike is a derived class which extends Bicycle class and class Test is a driver class to run program.

```java
//Java program to illustrate the 
// concept of inheritance 

// base class 
class Bicycle 
{ 
	// the Bicycle class has two fields 
	public int gear; 
	public int speed; 
		
	// the Bicycle class has one constructor 
	public Bicycle(int gear, int speed) 
	{ 
		this.gear = gear; 
		this.speed = speed; 
	} 
		
	// the Bicycle class has three methods 
	public void applyBrake(int decrement) 
	{ 
		speed -= decrement; 
	} 
		
	public void speedUp(int increment) 
	{ 
		speed += increment; 
	} 
	
	// toString() method to print info of Bicycle 
	public String toString() 
	{ 
		return("No of gears are "+gear 
				+"\n"
				+ "speed of bicycle is "+speed); 
	} 
} 

// derived class 
class MountainBike extends Bicycle 
{ 
	
	// the MountainBike subclass adds one more field 
	public int seatHeight; 

	// the MountainBike subclass has one constructor 
	public MountainBike(int gear,int speed, 
						int startHeight) 
	{ 
		// invoking base-class(Bicycle) constructor 
		super(gear, speed); 
		seatHeight = startHeight; 
	} 
		
	// the MountainBike subclass adds one more method 
	public void setHeight(int newValue) 
	{ 
		seatHeight = newValue; 
	} 
	
	// overriding toString() method 
	// of Bicycle to print more info 
	@Override
	public String toString() 
	{ 
		return (super.toString()+ 
				"\nseat height is "+seatHeight); 
	} 
	
} 

// driver class 
public class Test 
{ 
	public static void main(String args[]) 
	{ 
		
		MountainBike mb = new MountainBike(3, 100, 25); 
		System.out.println(mb.toString()); 
			
	} 
} 
```

> **Output:**
>
> No of gears are 3
> speed of bicycle is 100
> seat height is 25

In above program, when an object of MountainBike class is created, a copy of the all methods and fields of the superclass acquire memory in this object. That is why, by using the object of the subclass we can also access the members of a superclass.  
Please note that during inheritance only object of subclass is created, not the superclass. For more, refer  [Java Object Creation of Inherited Class](https://www.geeksforgeeks.org/gfact-52-java-object-creation-of-inherited-classes/).  
**Illustrative image of the program:**  
[![f](https://media.geeksforgeeks.org/wp-content/uploads/inheritence1.png "Click to enlarge")](https://media.geeksforgeeks.org/wp-content/uploads/inheritence1.png)

In practice, inheritance and  [polymorphism](https://www.geeksforgeeks.org/overriding-in-java/)  are used together in java to achieve fast performance and readability of code.

**Types of Inheritance in Java**

Below are the different types of inheritance which is supported by Java.

1.  **Single Inheritance :** In single inheritance, subclasses inherit the features of one superclass. In image below, the class A serves as a base class for the derived class B.
    
    [![Single_Inheritance](https://media.geeksforgeeks.org/wp-content/uploads/inheritance1.png "Click to enlarge")](https://media.geeksforgeeks.org/wp-content/uploads/inheritance1.png)
    
```java
//Java program to illustrate the 
// concept of single inheritance 
import java.util.*; 
import java.lang.*; 
import java.io.*; 

class one 
{ 
	public void print_geek() 
	{ 
		System.out.println("Geeks"); 
	} 
} 

class two extends one 
{ 
	public void print_for() 
	{ 
		System.out.println("for"); 
	} 
} 
// Driver class 
public class Main 
{ 
	public static void main(String[] args) 
	{ 
		two g = new two(); 
		g.print_geek(); 
		g.print_for(); 
		g.print_geek(); 
	} 
} 

```

>    **Output:**
>     
>    Geeks
>    for
>    Geeks

    
  

  
## Multilevel Inheritance
 In Multilevel Inheritance, a derived class will be inheriting a base class and as well as the derived class also act as the base class to other class. In below image, the class A serves as a base class for the derived class B, which in turn serves as a base class for the derived class C. In Java, a class cannot directly access the [grandparent’s members](https://www.geeksforgeeks.org/g-fact-91/).
    
    [![Multilevel_Inheritance](https://media.geeksforgeeks.org/wp-content/uploads/inheritance3.png "Click to enlarge")](https://media.geeksforgeeks.org/wp-content/uploads/inheritance3.png)