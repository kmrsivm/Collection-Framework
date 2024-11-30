## Vector 

Vector is like the dynamic array which can grow or shrink its size. Unlike array, we can store n-number of elements in it as there is no size limit. It is a part of Java Collection framework since Java 1.2. It is found in the java.util package and implements the List interface, so we can use all the methods of List interface here.

### Vector: Synchronized

Key Points:

	•	Thread Safety: Synchronized but slower.
	•	Growth Rate: Doubles its size when full.
	•	Performance: Best suited for multi-threaded environments where thread safety is required.

 	1.	Data Storage:
	•	A Vector internally uses a dynamic array (Object[] elementData) to store its elements.
	2.	Initial Capacity:
	•	When a Vector is created, it has an initial capacity (default: 10).
	3.	Capacity Expansion:
	•	If the current array is full, the Vector increases its capacity by 100% of its current size (i.e., doubles the array size).
	4.	Element Addition:
	•	When you add an element:
	•	If there’s space, the element is added at the next available index.
	•	If the array is full, the Vector creates a new array with increased capacity and copies all existing elements into the new array before adding the new element.
	5.	Synchronization:
	•	All methods in Vector (like add(), remove(), get()) are synchronized, making it thread-safe but slower compared to ArrayList.
	6.	Element Access:
	•	Elements are accessed by index, just like an array. The time complexity for accessing an element is O(1).
	7.	Iteration:
	•	Supports both:
	•	Enumeration (legacy iterator).
	•	Iterator for traversing the elements.
