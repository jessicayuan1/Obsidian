[[2024-01-23 Linked List]]
[[ECE 250 Data Structures and Algorithms]]

A set is good at detecting duplicates: 

Iterate through the linekd list, for each node, check if the set contains the data 
	No-> First time encounter, add to the set
	Yes -> duplicate found, remove it
	- Big O depends on efficiency of set.contain() operation


Insert log time chart here 

### Queue Implementation with Array
	head = 0
	tail = 0
	data {};

- Update head and tail as you enqueue and dequeue
- Tail has to wrap around to 0
- Increment by modding the array size
	(a + 1) % b
- 

### Queue Implementation with Linked List
	Enqueue at one end, dequeue at the other
* removefromFront O(1)
* addtoBack O (1) with tail pointer

### Deques 
	Ability to add/remove from both ends of the queue
	- Double ended queue

