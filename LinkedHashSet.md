## LinkedHashSet in Java

A LinkedHashSet is a hybrid data structure that combines the best of both worlds: the efficient lookup of a HashSet and the ordered nature of a LinkedList. It stores elements in the order they were inserted, while ensuring uniqueness.

Key Characteristics:

	1.	Ordered: Elements are stored in the order they were inserted.
	2.	Unique: Duplicate elements are not allowed.
	3.	Efficient: Uses a hash table internally for fast lookup.
	4.	Doubly-Linked List: Maintains a doubly-linked list to preserve insertion order.

 How it Works:

	1.	Hashing: When an element is added, its hash code is calculated to determine its position in the underlying hash table.
	2.	Linked List Insertion: The element is then added to the end of a doubly-linked list, ensuring that the insertion order is maintained.
	3.	Duplicate Check: The hash table is used to quickly check for duplicates. If a duplicate is found, it’s not added to the LinkedHashSet.

 Common Operations:

	1.	add(element): Adds an element to the LinkedHashSet.
	2.	remove(element): Removes an element from the LinkedHashSet.
	3.	contains(element): Checks if an element exists in the LinkedHashSet.
	4.	size(): Returns the number of elements in the LinkedHashSet.
	5.	isEmpty(): Checks if the LinkedHashSet is empty.
	6.	clear(): Removes all elements from the LinkedHashSet.
	7.	iterator(): Returns an iterator to iterate over the elements in insertion order.
 Use Cases:

	1.	Maintaining Insertion Order:
	•	When you want to store elements in the order they were added.
	2.	Unique Elements with Order:
	•	When you need a collection of unique elements that preserves the insertion order.
	3.	Caching:
	•	To implement caches that evict elements based on least recently used (LRU) or first-in-first-out (FIFO) policies.
 In Essence:

	•	LinkedHashSet offers a flexible and efficient way to store unique elements while maintaining their original insertion order.
