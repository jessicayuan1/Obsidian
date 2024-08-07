[[Binary Trees]]


Node's height is the mac number of nodes that can be reach from that node in one path.
Node's depth number of traversed nodes between the root and that node 

```cpp
template<class Type>
class binary_search_treeP
private:
	struct node{
	Type data;
	node* left
	node* right;
	node (Type d, node*l= nullptr, node*r = nullptr):
	data(d), left(l), right(r) {}
  }*root;
public:
	node*&search (const Type& item) {
		return search_internal(root, item);
	}

	bool insert (const Type& item){ //You get a pointer to that node
		node *& found_node = search(item);
		if (found_node == nullptr) {
		found_node = new node(item);
		return true
		}
	  return false

	}


	bool remove (const Type& item) {
		node *& found_node = search(item);
		if (found_node != nullptr) // if found exists, delete it
			deleteNode(found_node);
			return true
		}
		return false
	}

private:
	node*& search_internal (node*& curr_node, const Type& item){
		
		if (curr_node->data == item)
			return curr_node;
		else if (curr_node -> data > item)
			return search_internal(curr_node->left, item);
		else 
			return search_internal(curr_node -> right, item);
			

	}

```