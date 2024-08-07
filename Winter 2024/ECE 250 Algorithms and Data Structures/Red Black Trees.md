[[Binary Trees]]
Follow four rules
1. Every node is either red orb lack
2. the root is black
3. if a node is red, its children must be black
4. every path from root -> NULL must have the same number of black nodes

- Always add as red
- If you cannot add a consecutive number, rotate 

Preventatives
- Turn parent node to red and change recolour kids to black node
- If grandparent is red -- violation
	- Rotate again
- 