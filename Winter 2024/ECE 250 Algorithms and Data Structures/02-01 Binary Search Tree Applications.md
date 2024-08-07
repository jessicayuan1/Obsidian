[[01-31 Tree Traversals]]
[[ECE 250 Data Structures and Algorithms]]

- O(log(n)) addition, search and removal
- Requires keys to be a totally orders type
- Each BST node will hold the data for one entry:
Other operations typically not part of a map or set 


##### Addition of valid entries in a binary tree
- smaller entries go to the left of the node
- set a new pointer for the newNode

Pointer to a pointer approach 
- start by pointing to root, (root is a pointer to the first node)
Adding to BST with recursion
	BSTs are naturally recursive data structures
	```
	
```
void add (int toAdd){

}

Node * add (Node * current, int toAdd) { //should be private

		Exercise

}
```

##### Removal of entries in a binary tree
1. Find the node
	a. Using binary search & pionter to node before
2. Pointer manipulation
	a. leaf node
	b. has one child

In general: Set pointer to null first before adding to child 

Removing nodes with 1 child after
	- Set the parent node's pointer to it's grandchild
- Removing nodes with grandchildren
- 