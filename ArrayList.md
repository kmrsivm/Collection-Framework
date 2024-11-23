# ArrayList Internal Working in Java

### An ArrayList is a resizable array implementation of the List interface.  
Its ability to grow and shrink dynamically is one of its key features.

---

## Key Features
- The elements from the old array are copied into the new array.
- The new array replaces the old one internally.
- **Growing** happens automatically when needed, but **shrinking** happens only when explicitly triggered via `trimToSize()`.

---

## Default Capacity
- **DEFAULT_CAPACITY**: The initial capacity is `10` if no specific capacity is provided during creation.

```java
ArrayList<Integer> list = new ArrayList<>();
```

## Custom ArrayList with Capacity

You can specify the initial capacity during creation:
```
ArrayList<Integer> list = new ArrayList<>(20);
```

## ArrayList Growth Formula

The capacity of an ArrayList increases dynamically using the formula:

New capacity = (old capacity * 3/2) + 1

## Example Calculation

	1.	( 10 \times 3/2 = 10 \times 1.5 = 15 )
	2.	Add 1 to the result: ( 15 + 1 = 16 )


## Memory Management

	-	Unused Capacity: When elements are removed, the array’s capacity remains unchanged until trimToSize() is called.

## Key Methods

	-	add(E e): Adds an element to the ArrayList.
	-	get(int index): Fetches an element by index.
	-	remove(int index): Removes an element at the specified index.
	-	size(): Returns the current size of the ArrayList.
	-	trimToSize(): Reduces the capacity to match the size of the ArrayList.
	-	ensureCapacity(int minCapacity): Ensures a minimum capacity for the ArrayList.

## Advantages of ArrayList

	-	Fast random access: Provides O(1) time complexity for get and set.
## Disadvantages of ArrayList

	-	Slower insertion and deletion: These operations have a time complexity of O(n) in the worst case.
	-	Consumes extra memory: Unused capacity may result in wasted memory until explicitly managed.

