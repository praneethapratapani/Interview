### ARRAYS 

They are stored contiguously, homogeneous

Declarations: 
- Simple array: int[] arrayname or int arrayname[]
- Multi dimensional array : datatype [][] arrayrefvariable; or datatype arrayrefvariable[][];
- Insertion: At end: O(1), At some index : O(n)
- Deletion: O(n);
- Access O(1);

ARRAYS CLASS:
    java.util.Arrays package should be imported

JAGGED ARRAYS:
    Every row has different number of columns



### LINKED LIST

Made of nodes consisting of data fields and pointer to next node

**Circular linked list** : if last node has a tail pointer and pointing it to first node , then it becomes circular linked list.

**Doubly linked list** : have three elements - pointer - data - pointer          

### STACK
push, pop, peek (sees first element without removing it) - LIFO

- push peek and pop - O[1]
- use stack while defining

### QUEUE

- push(enqueue), pop(dequeue), peek (follows LIFO), poll (removes head or returns null if no head,follows FIFO) - FIFO   
- enqueue - q.offer(param),dequeue - q.poll() and poll - O(1)
use linkedlist while defining

### TREES 

- inorder : left - current node - right
- pre order : current node - left - right
- post order: left - right - current 
 
**Binary search tree** - all left subtree values are less than node's value & right side nodes are greater than node's value
**Binary tree**
- has only one root
- has exactly one path b/w root and any node
- any node will have atmost 2 children

**Balanced binary tree** -  A binary tree where the height difference between the left and right subtrees of any node is at most 1.


### SETS 
only have unique elements, hashcodes are returned as position or index. Sets are used to store unique elements and check for the existence of specific values.

### MAPS 

Stores key-value pairs, no two keys can be repeated and each key has only one value. Maps are used to associate keys with values and perform lookup operations based on keys.

- Keyset() function will give you all the keys present in hashmap 
- get(key) - will give you value present at key
- put() - will add

**TIME COMPLEXITY**
- Access: O(1) (for arrays, hash-based structures)
- Insertion/Deletion:
- O(1) (for stacks, queues, hash-based structures)
- O(n) (for linked lists, arrays - at arbitrary position)
- Traversal/Searching: O(n) (for trees, linked lists)
- Insertion/Deletion/Searching (on average):
- O(log n) (for balanced binary search trees)
- O(1) (for hash-based structures) 