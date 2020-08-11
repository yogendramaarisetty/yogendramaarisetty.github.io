# Message Passing in Java


**What is message passing and why it is used?**  
Message Passing in terms of computers is communication between processes. It is a form of communication used in object-oriented programming as well as parallel programming. Message passing in Java is like sending an object i.e. message from one thread to another thread. It is used when threads do not have shared memory and are unable to share monitors or semaphores or any other shared variables to communicate. Suppose we consider an example of producer and consumer, likewise what producer will produce, the consumer will be able to consume that only. We mostly use  **[Queue](http://www.geeksforgeeks.org/queue-data-structure/)**  to implement communication between threads.

![](https://media.geeksforgeeks.org/wp-content/uploads/20190509121341/Message-Passing-in-Java-1024x634.jpg "Click to enlarge")

In the example explained below, we will be using vector(queue) to store the messages, 7 at a time and after that producer will wait for the consumer until the queue is empty.

In Producer there are two synchronized methods  **putMessage()**  which will call form  **run()**  method of Producer and add message in Vector whereas  **getMessage()**  extracts the message from the queue for the consumer.

Using message passing simplifies  [the producer-consumer problem](https://www.geeksforgeeks.org/producer-consumer-solution-using-threads-java/)  as they don’t have to reference each other directly but only communicate via a queue.

**Example:**

```java
import java.util.Vector; 

class Producer extends Thread { 

	// initialization of queue size 
	static final int MAX = 7; 
	private Vector messages = new Vector(); 

	@Override
	public void run() 
	{ 
		try { 
			while (true) { 

				// producing a message to send to the consumer 
				putMessage(); 

				// producer goes to sleep when the queue is full 
				sleep(1000); 
			} 
		} 
		catch (InterruptedException e) { 
		} 
	} 

	private synchronized void putMessage() 
		throws InterruptedException 
	{ 

		// checks whether the queue is full or not 
		while (messages.size() == MAX) 

			// waits for the queue to get empty 
			wait(); 

		// then again adds element or messages 
		messages.addElement(new java.util.Date().toString()); 
		notify(); 
	} 

	public synchronized String getMessage() 
		throws InterruptedException 
	{ 
		notify(); 
		while (messages.size() == 0) 
			wait(); 
		String message = (String)messages.firstElement(); 

		// extracts the message from the queue 
		messages.removeElement(message); 
		return message; 
	} 
} 

class Consumer extends Thread { 
	Producer producer; 

	Consumer(Producer p) 
	{ 
		producer = p; 
	} 

	@Override
	public void run() 
	{ 
		try { 
			while (true) { 
				String message = producer.getMessage(); 

				// sends a reply to producer got a message 
				System.out.println("Got message: " + message); 
				sleep(2000); 
			} 
		} 
		catch (InterruptedException e) { 
		} 
	} 

	public static void main(String args[]) 
	{ 
		Producer producer = new Producer(); 
		producer.start(); 
		new Consumer(producer).start(); 
	} 
} 

```

> **Output:**
> 
> Got message: Thu May 09 06:57:53 UTC 2019 Got message: Thu May 09
> 06:57:54 UTC 2019 Got message: Thu May 09 06:57:55 UTC 2019 Got
> message: Thu May 09 06:57:56 UTC 2019 Got message: Thu May 09 06:57:57
> UTC 2019 Got message: Thu May 09 06:57:58 UTC 2019 Got message: Thu
> May 09 06:57:59 UTC 2019 Got message: Thu May 09 06:58:00 UTC 2019
