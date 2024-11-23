## Linked list Internal Working

- Linked list is a dynamic data structure that stores elements in a linear fashion, where each element (node) contains a value and a reference to the next node in the list. Unlike arrays, linked lists don't require contiguous memory allocation, making them efficient for insertions and deletions.


## Key Features

	-	Each element (called a node) contains:
	-	A reference to the next node.
	-	A reference to the previous node.
	-	LinkedList is doubly linked, meaning each node points to both its previous and next nodes.
	-	It supports null values and duplicates.

```
	private static class Node<E> {
    		E item;       // Data of the node
   		 Node<E> next; // Reference to the next node
   		 Node<E> prev; // Reference to the previous node

    		Node(Node<E> prev, E element, Node<E> next) {
			this.item = element;
        		this.next = next;
        		this.prev = prev;
    		}
	}
```

## Key Methods

	-	add(E e): Adds an element to the end of the list.
	-	addFirst(E e) / addLast(E e): Adds an element to the beginning or end.
	-	remove(int index): Removes the element at the specified index.
	-	get(int index): Retrieves the element at the specified index.
	-	size(): Returns the number of elements.
	-	isEmpty(): Checks if the list is empty.

## Advantages of LinkedList

	-	Efficient insertion and deletion:
	-	O(1) for adding/removing at the start or end.
	-	O(n) for adding/removing at a specific index.
	-	No resizing overhead as in an ArrayList.

## Disadvantages of LinkedList

	-	Slower random access:
	-	O(n) for accessing elements by index.
	-	Higher memory usage:
	-	Each node requires extra memory for prev and next pointers.


## ArrayList vs LinkedList

```
	Feature	ArrayList				LinkedList
	Memory usage					Less (no pointers)	More (pointers needed)
	Access time (get())				Fast (O(1))	Slow (O(n))
	Insertion/Deletion				Slow (O(n))	Fast (O(1) at ends)
	Resizing overhead				Present	Absent
```
