[[ECE 250 Data Structures and Algorithms]]

In summary: Iterating through trees


Starting with in order
* Traverse left subtree (recurse left)
* Print out value
* Traverse right subtree (recurse right)

Pseudocode:

```
Create Stack s
Set curr as the root 
While s is not empty or curr is not NULL
	while curr is not NULL:
	s.push (curr)
	curr  = curr-> left
curr = s.pop()
process curr
curr = curr -> right
```
	Once finished with a branch, pop the leaf from the stack 


Pre-order Traversal
- Useful for dependency resolution
- Process  children first, then yourself



Level-order Traversal
- Root first
- Children
- Grandchildren
Iterating tracking can use a Queue, FIFO
```
Create Queue q
Add root to q
while q is not empty:
Node curr = q.dequeue()
if curr-> left is not NULL:
	q.enqueue(curr->left)
if curr->right is not NULL:
q.enqueue(curr-> right)
```

Remember: a tree is a type of graph
