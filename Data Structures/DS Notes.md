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

### PRIORITY QUEUE OR HEAP
should follow 3 conditions
  1. Binary tree - every node has atmost 2 children
  2. Heap Invariant - every node is less(min)/greater(max) or equal to its children
  3. Always a complete tree
most important first out
- min heap 
- max heap 

peekMin() - O(1)
removeMin() - bubbledown : will choose smallest child and swap till end.  O(1) for removing last node + O(h) for bubble down
for a complete tree - log n is height
add() - implement bubbleup after adding the element to make it balanced (mostly in the left subtree)

so, for remove and add - best is O(1) and worst is O(log n)
in practice - remove is O(log n) and add is O(1)
Heap using array 
see notes

### TREES 
 
 ```
    class Node{
        int val;
        Node left,right;

        public Node(int item){
            val = item;
            left = right = null;
        }
    }
 ```
**Binary search tree** - all left subtree values are less than node's value & right side nodes are greater than node's value

insert,delete and search - O(n) 

**Binary tree**
- has only one root
- has exactly one path b/w root and any node
- any node will have atmost 2 children
- empty tree is also an binary tree

**Balanced binary tree** -  A binary tree where the height difference between the left and right subtrees of any node is at most 1.
insert,delete and search - O(log n) base 2

### SETS 
only have unique elements, hashcodes are returned as position or index. Sets are used to store unique elements and check for the existence of specific values.

**Disjoint Set Data Structure**
any sets which does not have any common element - uses union

Union by size - O(log n) - point smaller tree to the root of larger tree 
- find will become O(1) - in best case and O(log n)in worst case
- 

Path Compression - almost O(1) - log* n
actual complexity is O(alpha(n)) - alpha(n) is called ackermann's function

![Alt text](<Simplified calculations to.png>)
### MAPS 

Stores key-value pairs, no two keys can be repeated and each key has only one value. Maps are used to associate keys with values and perform lookup operations based on keys.

- Keyset() function will give you all the keys present in hashmap 
- get(key) - will give you value present at key
- put() - will add

### GRAPHS
- Tree is a subset of graph - acyclic undirected graph
- uses set i.e., set(vertices,edges)
- any vertex can be connected to any vertex (nodes are vertices)
- if there are n vertices, each vertex have n-1 edges
- for undirected graph, total edges = n(n-1)/2
- for directed graph, total edges = n(n-1)
- if it has self loop then n2 edges 
- dense graph - almost all edges are connected to each other
- sparse graph - few are connected to each other
- Path : is sequence of vertices where each vertex is connected via edge.
- simple path - vertices are not repeated
- cycle is like a loop
- adjacency matrix - 1 is assigned when there is edge and 0 when there is no edge.
- adjacency list is used for saving memory

**Directed Graph** - has directions between vertices

**Undirected Graph** - just and edge represents the connection - like a double sided arrow
Ex: social network - if you are friend of them then they are friend of yours - like facebook.

### DYNAMIC PROGRAMMING

1. an optimal substructure property (recursion)
2. overlapping sub problems

Two variants
    - Bottom up dynamic programming - Time O(n),Space - O(n)
    - memoization - it does not resolve already calculated sub part, it takes from the table stored - Time O(n),Space - O(n)

### Minimum Spanning Tree
is a subgraph of an undirected weighted graph G, such that
- its a tree (acyclic)
- it covers all the vertices V
  - contains V-1 edges
- total cost associated with tree edges is the minimum among all possible spanning trees.
- may not be unique.

### TRIE
came from word re'trie've.

- Each trie has a root node
- each node is a string and each edge is a character

```
    public class TrieNode{
        public char val;
        public TrieNode[] children;
        public boolean isWord;

        public TrieNode(char c){
            val = c;
            children = new TrieNode[26]; // For alphabets
            isWord = false;
        }
    }
```

Complexities
Insertion - O(n), O(n*m)
Deletion - O(n) ,O(1)
Search - O(n), O(1)
**TIME COMPLEXITY**
- Access: O(1) (for arrays, hash-based structures)
- Insertion/Deletion:
- O(1) (for stacks, queues, hash-based structures)
- O(n) (for linked lists, arrays - at arbitrary position)
- Traversal/Searching: O(n) (for trees, linked lists)
- Insertion/Deletion/Searching (on average):
- O(log n) (for balanced binary search trees)
- O(1) (for hash-based structures) 