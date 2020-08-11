# Abstraction in Java


Data Abstraction is the property by virtue of which only the essential details are displayed to the user.The trivial or the non-essentials units are not displayed to the user. Ex: A car is viewed as a car rather than its individual components.

Data Abstraction may also be defined as the process of identifying only the required characteristics of an object ignoring the irrelevant details.The properties and behaviors of an object differentiate it from other objects of similar type and also help in classifying/grouping the objects.

Consider a real-life example of a man driving a car. The man only knows that pressing the accelerators will increase the speed of car or applying brakes will stop the car but he does not know about how on pressing the accelerator the speed is actually increasing, he does not know about the inner mechanism of the car or the implementation of accelerator, brakes etc in the car. This is what abstraction is.

In java, abstraction is achieved by  [interfaces](https://www.geeksforgeeks.org/interfaces-in-java/)  and  [abstract classes](https://www.geeksforgeeks.org/abstract-classes-in-java/). We can achieve 100% abstraction using interfaces.

**Abstract classes and Abstract methods :**	
1.  An abstract class is a class that is declared with  [abstract keyword.](https://www.geeksforgeeks.org/abstract-keyword-in-java/)
2.  An abstract method is a method that is declared without an implementation.
3.  An abstract class may or may not have all abstract methods. Some of them can be concrete methods
4.  A method defined abstract must always be redefined in the subclass,thus making  [overriding](http://contribute.geeksforgeeks.org/overriding-in-java/)  compulsory OR either make subclass itself abstract.
5.  Any class that contains one or more abstract methods must also be declared with abstract keyword.
6.  There can be no object of an abstract class.That is, an abstract class can not be directly instantiated with the  _[new operator](https://www.geeksforgeeks.org/new-operator-java/)_.
7.  An abstract class can have parametrized constructors and default constructor is always present in an abstract class.

**When to use abstract classes and abstract methods with an example**

There are situations in which we will want to define a superclass that declares the structure of a given abstraction without providing a complete implementation of every method. That is, sometimes we will want to create a superclass that only defines a generalization form that will be shared by all of its subclasses, leaving it to each subclass to fill in the details.

Consider a classic “shape” example, perhaps used in a computer-aided design system or game simulation. The base type is “shape” and each shape has a color, size and so on. From this, specific types of shapes are derived(inherited)-circle, square, triangle and so on – each of which may have additional characteristics and behaviors. For example, certain shapes can be flipped. Some behaviors may be different, such as when you want to calculate the area of a shape. The type hierarchy embodies both the similarities and differences between the shapes.

![](https://media.geeksforgeeks.org/wp-content/uploads/Abstract-classes-and-methods-Page-1.png "Click to enlarge")
```java
// Java program to illustrate the 
// concept of Abstraction 
abstract class Shape 
{ 
	String color; 
	
	// these are abstract methods 
	abstract double area(); 
	public abstract String toString(); 
	
	// abstract class can have constructor 
	public Shape(String color) { 
		System.out.println("Shape constructor called"); 
		this.color = color; 
	} 
	
	// this is a concrete method 
	public String getColor() { 
		return color; 
	} 
} 
class Circle extends Shape 
{ 
	double radius; 
	
	public Circle(String color,double radius) { 

		// calling Shape constructor 
		super(color); 
		System.out.println("Circle constructor called"); 
		this.radius = radius; 
	} 

	@Override
	double area() { 
		return Math.PI * Math.pow(radius, 2); 
	} 

	@Override
	public String toString() { 
		return "Circle color is " + super.color + 
					"and area is : " + area(); 
	} 
	
} 
class Rectangle extends Shape{ 

	double length; 
	double width; 
	
	public Rectangle(String color,double length,double width) { 
		// calling Shape constructor 
		super(color); 
		System.out.println("Rectangle constructor called"); 
		this.length = length; 
		this.width = width; 
	} 
	
	@Override
	double area() { 
		return length*width; 
	} 

	@Override
	public String toString() { 
		return "Rectangle color is " + super.color + 
						"and area is : " + area(); 
	} 

} 
public class Test 
{ 
	public static void main(String[] args) 
	{ 
		Shape s1 = new Circle("Red", 2.2); 
		Shape s2 = new Rectangle("Yellow", 2, 4); 
		
		System.out.println(s1.toString()); 
		System.out.println(s2.toString()); 
	} 
} 

```

> **Output:**
> 
> Shape constructor called Circle constructor called Shape constructor
> called Rectangle constructor called Circle color is Redand area is :

 15.205308443374602
    Rectangle color is Yellowand area is : 8.0
   **Encapsulation vs Data Abstraction**

1.  [Encapsulation](http://contribute.geeksforgeeks.org/encapsulation-in-java/)  is data hiding(information hiding) while Abstraction is detail hiding(implementation hiding).
2.  While encapsulation groups together data and methods that act upon the data, data abstraction deals with exposing the interface to the user and hiding the details of implementation.

**Advantages of Abstraction**

1.  It reduces the complexity of viewing the things.
2.  Avoids code duplication and increases reusability.
3.  Helps to increase security of an application or program as only important details are provided to the user.