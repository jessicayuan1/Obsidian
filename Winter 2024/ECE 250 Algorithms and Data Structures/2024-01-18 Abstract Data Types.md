[[ECE 250 Data Structures and Algorithms]]
* Separation of interface from implementation
* Doing something without needing to know the intricacies 


Interface is an abstraction type

# Queues
FIFO

- primary operations: **enqueue and dequeue**
- FIFO -> Iterms returns by dequeue are in the same order as dequeue

## Uses
* Hardware: instruction queues in processors, packet queues in networks, etc
* Task scheduling, BFS
* Natural choice for fairness in lineups

## ADT Definition

```
tempalte <typename T>
class Queue {
	void enqueue (const T & item); // Add code here to define it using arrays and index
	T dequeue(); //can return void
	T & peek();
	const T & peek() const;
	int numItems() const;
}

// STL has a std queueu class with different functnions names.

```

# Stacks
1. LIFO
2. push and pop

## Uses
- Function call stack
- Copy and Paste clipboard
- Reverse sequence of items 
- Bracket matching in compiler 

const is a direct reference, no modifying 
# Sets
* a collection of elements 
	* Supports operations similar to those found on a mathematical set
		* Add item, test if it in t
		* Union, intersection
	* Only 1 instance of each element 

## Uses
* Tracking what items belong to a particular group
	* In a word based game: track valid words
	* If two tasks are scheduled at the same time 

# Maps
* Tracks a mapping from **keys** to **values**
* Operations:
	* Add
	* Lookup
	* NumItems
	* Remove
* If had iterator: return key value pair 
