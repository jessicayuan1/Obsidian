[[ECE 250 Data Structures and Algorithms]]

## Operations
Adding three to the top of the list
* Create a new node
* Let data be 3
* Make it's next be head
* point head towards the node we made for 3

Adding to the back
* New node, set data to 3 <- O(1)
* Point 3 to null <- O(1)
* Point the current last node's next to 3 
	* Traverse through the entire linked list O(n)
* With a tail pointer, you have access to the current last node 
	* tail-> = new_node O(1)

Removal of 3 from the front of the list
* Update head pointer to the second node
	* Need to use a temp pointer so that you don't lose track of the node
	* "Store head in a temp pointer"
* Delete the node using temp
	* In C++ manually manage memory
	* Then set temp to null 

Removing from the back
- Delete the last node
	- Iterate through the entire linked list O(n)
	- Tail pointer only gives the last node, not the second last node that we need access to to manage the pointing to the last
- Set second last's next to null 

## Searching 

#### Inserting in sorted order 
	Inserting 5 between 4 and 7
- Searching for the node before using a "current pointer "
	* data(5) <   curr->next->data    // 
* Once found using condition
	* Create new node
	* Set data to 5
	* Set next to curr->next (current pointer's next is pointing to 7)
Corner case inserting item at the front (?)
* make a new node
* point it to 3
* head = new Node(data, head)
What do they both have in common?
* Corner - changed head
* Common - change the next firled
* Both node *
* Node * * is a pointer to a pointer 
	* The box we are looking at 
	* Requires more pointer understanding 

Pointer to pointer approach
	Insert 5 between 4 and 7 still
* curr starts pointing at head, where head points to the first element of the list
* when you get value of curr, you get head,  which is a pointer to a node
	* So curr is node **
	* start it at &head 
	*Note: a pointer is something's address
	* As we search, curr changes to pointing to something's next field
	* Looking for -- when (*current)-> data > data(5)
	* Advance curr, then the next is pointing towards 7
		* Now make a new Node with data = 5, next = 7
		* ** curr gives us the node, *current gives the pointer to a node 
	* Set 4's next towards 5 now 

Now to insert 2 at the front 
	Current is pointing to head which is pointing to next (curr**)
	Make a new Node with data =2, next = *current

[[Recursive approach]]
NEXT CLASS
	
