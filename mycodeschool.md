
# ADT - abstract data type

# linear data structure
## list
1. one byte of memory has an address, one integer requires 4 bytes, 32 bits
2. programmer use programming language to talk to memory, address of the block of memory is the address of first byte
3. In C, array created using "malloc", we can use "realloc" to re-size it. Some memory block may be extended if space adjacent to the block is available.

## linked-list
```
struct Node {
  int data;
  struct Node* next;
};
```
1. are collections of entities that we call nodes.
2. one memory block saves data value, one memory block saves address for next node
3. The identity of a linked list is the reference/address to the head node. address of the head node gives us access of the complete list, we need a variable to save the pointer to the head node.
4. tail address pointer will save 0/null


## doubly linked-list
```
struct Node {
  int data;
  struct Node* next;
  struct Node* prev;
};
```

## stack
1. property, constrant / restriction: items must be inserted or removed from the same end that we call the top of stack.
2. last-in-first-out
3. operation: O(1)
* insertion: push
* deletion: pop
* return the first ele: top
* check: isEmpty()
4. application:
* function calls / recursion
* undo operation
* balabced parentheses

## queue
1. insertion from rear/tail of the queue, removal from front/head of the queue
2. first-in-first-out
3. operation: O(1)
* insertion: enqueue/push, 
* removal: dequeue/pop, returns the element
* front() / peek(): return the front element
* isEmpty()
4. application: shared source, can serve 1 request at  1 time
* printer queue
* process scheduling
* simulating

# non-linear
## tree
1. a collection of entities called nodes linked together to  simulate a heirachy
2. link is one direction, sibling and cousion
3. property
* recursive data structure
* N nodes -- N-1 edges
* depth of Node x: length of path from root to x
* height of Node x: number of edges in longest length from x to a leaf
4. application:
* store naturally hirarchical data -> file system
* organizing data for quick search, insertion, deletion -> binary search tree
* tire -> dictionary
* network routing algorithm

## binary tree -- each node can have at most 2 children, left child, rigth child
```
struct Node {
  int data;
  Node* left;
  Node* right;
}
```

1. type
* strict/proper binary tree: each node can have either 2 or 0 children
* complete binary tree: all levels except possibly the last are completely filled and all nodes are as left as possible
* perfect binary tree: all levels are complete

2. maximum number of nodes in a tree with height n: 2^(n+1)-1
3. height of a perfect binary tree: log(n+1)-1
height of a complete binary tree: `[logN]`

4. cost of operation on tree is proportional to the height of tree. -- keep a tree balanced, minimize height

for a tree with N nodes, the minimum height is `floor(logN`), the maximum height is `N-1`

5. balanced binary tree: difference between height of left and right subtree for every node is no more than k (mostly 1)

height of empty tree is -1, height of tree of 1 node is 1

6. implementation
1) dynamically allocated nodes
2) array: complete binary tree -- for node at index N, left child will be at index 2N+1, right child will be at index 2N+2
* heap is a special binary tree, is implement by array

## binary search tree
1. the cost of a sorted array is `logN`
<img src="https://github.com/zhaaaa7/data-structure/blob/master/img/bigO.png" width="700px" />

2. all nodes in left subtree is <= Node, in right subtree is >=Node

3. **seach space will be reduced to** n/2 each time, and finaaly reach 1, that is 
```
n/(2^k)=1 => k=logn
```

4. balanced tree becomes unbalance during insertion and deletion, so we need to restore is

## graph
1. no rules for connection
```
G=(V,E) //ordered pair
```
edge is identified by its two end

2. edges:
* directed: `(u,v)`
* undirected: `{u,v}`

3. directed graph and undirected graph
weighted/unweighted graph


4. application: represent collection of objects having some kind of pairwise relationship
* social network
* web crawling: graph traversal
* inter-city road network

5. properties
* simple graph: graph with no self-loop,multi-edge
* max edge for directed graph: `0<=|E|<=n(n-1)`, min edge for directed graph: `0<=|E|<=n(n-1)/2`
* dense/sparse graph
* walk: a sequence of vertices where each adjacent pair is connected by an edge

path: a walk in which no vertices(thus no edges) are not repeated

trail: a trail in which ni edges are not repeated

closed walk: starts and ends at same vertex

simple cycle: no other vertixes is repeated

acyclic graph: a graph with no cycle


* strongly connected graph: if there is a path from any vertex to any other vertex

weakly connected: if it can be stronly connected if ignoring direction

# implementation

## BST
1. All nodes will be created in dynamic memory or heap section of application memory using malloc function. They cannot have ha name or identifier. They have to be accessed through a pointer.
