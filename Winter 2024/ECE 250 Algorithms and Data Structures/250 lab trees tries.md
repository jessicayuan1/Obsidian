```
valgrind -s --error-exitcode=1 --leak-check=yes --exit-on-first-error=yes ./spellcheck.out < ./inputs/50k.in


```
```valgrind -s --error-exitcode=1 --leak-check=yes --exit-on-first-error=yes ./spellcheck.out < ./inputs/50k.in

```cpp
	//Erase
	
	Node* current = root;
    Node* previous = root;
    Node* temp = nullptr;
    int index = 0;
    while (*word) {
       index = *word - 'a';
       if (!current->alphabet[index]) {
           return;
       }
       previous = current;
       current = current->alphabet[index];
       word++;
    }
    if (current->done) {
       current->done = false;
       count--;
    }
    for (int i = 0; i < 26; i++) {
       if (current->alphabet[i]) {
           return;
       }
    }
    delete current;
    current = nullptr;
    previous->alphabet[index] = nullptr;
    count--;
    return;
```



```cpp

#include "trie.h"
#include <string>
#include <iostream>

// implement classes' member functions here...



Trie::Trie(){
    root = new Node();
    // letters = new Node[26];
    count = 0;
};

    //Traverse the trie to locate the node correspoinding to the string to be deleted and remove it. 
    //If the removal of a node leaves it's parent node with no other childrem it may also need to be removed recursively.

    void Trie::erase(std::string word) {
        eraseHelper(root, word, 0);
    };

    void Trie::eraseHelper(Node* node, std::string word, int index) {
        if (index == word.length()) {
            if (node->done) {
                node->done = false;
                count--;
            }
            if (nochildren(node)) {
                delete node;
                node = nullptr;
            }
            return;
        }
        int childIndex = word[index] - 'a';
        if (node->alphabet[childIndex] == nullptr) {
            return;
        }
        eraseHelper(node->alphabet[childIndex], word, index + 1);
        if (nochildren(node->alphabet[childIndex])) {
            delete node->alphabet[childIndex];
            node->alphabet[childIndex] = nullptr;
        }
    };

    
   


int Trie::checksize(){
    return count;
};

bool Trie::nochildren(Node* node) {
    for (int i = 0; i < 26; ++i) {
        if (node->alphabet[i] != nullptr)
            return false;
        }
    return true;
}

void Trie::spellcheck(std::string word) {
        Node* current = root;
        int index = 0;

        while (index < word.length()) {
            int letterindex = word[index] - 'a';
            if (current->alphabet[letterindex] == nullptr) {
                // Node corresponding to the string does not exist
                return;
            }
            current = current->alphabet[letterindex];
            index++;
        }

        if (!current->done) {
            // Node corresponding to the string does not exist
            return;
        }

        current->done = false;
        count--;

    };


void Trie::insert( std::string word ) {

    Node*current = root;

    for (char& c : word) {
            int index = c - 'a';      // Subtract to get index
            if (!current->alphabet[index]) {//If the letter is not in the trie
                current->alphabet[index] = new Node();//Create a new node
            }
            current = current->alphabet[index]; //Move to the next node
        }
    
    if (current->done == true) { // If the word already exists in the trie
        std::cout << "failure" << std::endl;
    } else {
        current->done = true;
        count++;
        std::cout << "success" << std::endl;
    }

};

    
void Trie::printall() {// Print all words in alphabetical order
        printallHelper(root);
};
void Trie::printallHelper(Node* node) {
    if (node == nullptr) {
        return;
    }
    if (node->done) {
        //Print the word without having the word stored

    }
    for (int i = 0; i < 26; ++i) {//Iterate through the alphabet
        if (node->alphabet[i] != nullptr) {//If the node is not null
            printallHelper(node->alphabet[i]); //Go depth first into the trie

            // std::cout << node->alphabet[i];

        
        }
    }
};



void Trie::countprefix(std::string word) {
    
    countprefixHelper(root, word, 0);

};
void Trie::countprefixHelper(Node* node, std::string word, int index) {
    if (index == word.length()) {
        return;
    }
    int childIndex = word[index] - 'a';
    if (node->alphabet[childIndex] == nullptr) {
        return;
    }
    countprefixHelper(node->alphabet[childIndex], word, index + 1);
};



void Trie::clear () {
    //Delete all words from the tree

    delete root;
    root = new Node();
    count = 0;

    std::cout << "success" << std::endl;
    
}

Trie::~Trie() {
    delete root;
};


```