# Methods in Java


A method is a collection of statements that perform some specific task and return the result to the caller. A method can perform some specific task without returning anything. Methods allow us to  **reuse**  the code without retyping the code. In Java, every method must be part of some class which is different from languages like C, C++, and Python.  
Methods are  **time savers** and help us to  **reuse**  the code without retyping the code.

**Method Declaration**

In general, method declarations has six components :

-   **Modifier**-: Defines  **access type**  of the method i.e. from where it can be accessed in your application. In Java, there 4 type of the access specifiers.
    -   public: accessible in all class in your application.
    -   protected: accessible within the class in which it is defined and in its  **subclass(es)**
    -   private: accessible only within the class in which it is defined.
    -   default (declared/defined without using any modifier) : accessible within same class and package within which its class is defined.
-   **The return type**  : The data type of the value returned by the method or void if does not return a value.
-   **Method Name**  : the rules for field names apply to method names as well, but the convention is a little different.
-   **Parameter list** : Comma separated list of the input parameters are defined, preceded with their data type, within the enclosed parenthesis. If there are no parameters, you must use empty parentheses ().
-   **Exception list** : The exceptions you expect by the method can throw, you can specify these exception(s).
-   **Method body** : it is enclosed between braces. The code you need to be executed to perform your intended operations.

![methods in java](https://media.geeksforgeeks.org/wp-content/uploads/methods-in-java.png "Click to enlarge")

**Method signature**: It consists of the method name and a parameter list (number of parameters, type of the parameters and order of the parameters). The return type and exceptions are not considered as part of it.  
Method Signature of above function:

 max(int x, int y) 

**How to name a Method?**: A method name is typically a single word that should be a  **verb**  in lowercase or multi-word, that begins with a  **verb**  in lowercase followed by  **adjective, noun…..** After the first word, first letter of each word should be capitalized. For example, findSum,  
computeMax, setX and getX

Generally, A method has a unique name within the class in which it is defined but sometime a method might have the same name as other method names within the same class as  [method overloading is allowed in Java](https://www.geeksforgeeks.org/overloading-in-java/).

**Calling a method**

The method needs to be called for using its functionality. There can be three situations when a method is called:  
A method returns to the code that invoked it when:

-   It completes all the statements in the method
-   It reaches a return statement
-   Throws an exception

```java
// Program to illustrate methodsin java 
import java.io.*; 

class Addition { 
	
	int sum = 0; 
	
	public int addTwoInt(int a, int b){ 
		
		// adding two integer value. 
		sum = a + b; 
		
		//returning summation of two values. 
		return sum; 
	} 
	
} 

class GFG { 
	public static void main (String[] args) { 
	
		// creating an instance of Addition class 
		Addition add = new Addition(); 
		
		// calling addTwoInt() method to add two integer using instance created 
		// in above step. 
		int s = add.addTwoInt(1,2); 
		System.out.println("Sum of two integer values :"+ s); 
		
	} 
} 

```

> **Output :**
> 
> Sum of two integer values :3

See the below example to understand method call in detail :
```java
// Java program to illustrate different ways of calling a method 
import java.io.*; 

class Test 
{ 
	public static int i = 0; 
	// constructor of class which counts 
	//the number of the objects of the class. 
	Test() 
	{ 
		i++; 
		
	} 
	// static method is used to access static members of the class 
	// and for getting total no of objects 
	// of the same class created so far 
	public static int get() 
	{ 
		// statements to be executed.... 
		return i; 
	} 

	// Instance method calling object directly 
	// that is created inside another class 'GFG'. 
	// Can also be called by object directly created in the same class 
	// and from another method defined in the same class 
	// and return integer value as return type is int. 
	public int m1() 
	{ 
		System.out.println("Inside the method m1 by object of GFG class"); 
		
		// calling m2() method within the same class. 
		this.m2(); 
		
		// statements to be executed if any 
		return 1; 
	} 

	// It doesn't return anything as 
	// return type is 'void'. 
	public void m2() 
	{ 

		System.out.println("In method m2 came from method m1"); 
	} 
} 

class GFG 
{ 
	public static void main(String[] args) 
	{ 
		// Creating an instance of the class 
		Test obj = new Test(); 
		
		// Calling the m1() method by the object created in above step. 
		int i = obj.m1(); 
		System.out.println("Control returned after method m1 :" + i); 
		
		// Call m2() method 
		// obj.m2(); 
		int no_of_objects = Test.get(); 
		
		System.out.print("No of instances created till now : "); 
		System.out.println(no_of_objects); 
		
	} 
} 

```

> **Output :**
> 
> Inside the method m1 by object of GFG class In method m2 came from
> method m1 Control returned after method m1 :1 No of instances created
> till now : 1

Control flow of above program:


![methods in java](https://media.geeksforgeeks.org/wp-content/uploads/methods-in-java2.png "Click to enlarge")

**Memory allocation for methods calls**

Methods calls are implemented through stack. Whenever a method is called a stack frame is created within the stack area and after that the arguments passed to and the local variables and value to be returned by this called method are stored in this stack frame and when execution of the called method is finished, the allocated stack frame would be deleted. There is a stack pointer register that tracks the top of the stack which is adjusted accordingly.

**Related articles:**

-   [Java is strictly pass by value](https://www.geeksforgeeks.org/g-fact-31-java-is-strictly-pass-by-value/)
-   [Method overloading and Null error in Java](https://www.geeksforgeeks.org/method-overloading-null-error-java/)
-   [Can we overload or override static methods in Java?](https://www.geeksforgeeks.org/can-we-overload-or-override-static-methods-in-java/)
-   [Java Quizzes](http://quiz.geeksforgeeks.org/quiz-corner/#Java%20Programming%20Mock%20Tests)

**  
Reference:**  [https://docs.oracle.com/javase/tutorial/java/javaOO/methods.html](https://docs.oracle.com/javase/tutorial/java/javaOO/methods.html)