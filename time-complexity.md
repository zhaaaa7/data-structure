https://classroom.udacity.com/courses/ud513/lessons/7123524086/concepts/71225249930923

## big O notation:
1. O(n): n refers to the length of the input of the function

2. talk about efficiency in worst case

3. approximation


## collection
1. no order

2. different type

### list
1. order
2. different type
3. no fixed length


#### Linked Lists
1. extension of lists, no indices, characterized by links
2. insertion and deletion is easy: O(1)

#### Doubly Linked Lists
1. two direction reversal



#### Array
1. index
2. access value is easy
3. insertion and deletion is messy: O(n)


#### difference between Array and Linked list
1. index <-> next(memory location)

#### stacks
1. like stacks in real life: Last In, First Out
2. useful when you care about the most recent elements
3. push() and pop(): O(1)
4. abstract, can be implement with other data types with adding and removing element

#### queue
1. First in, First Out
2. Head <->.... <->Tail
3. dequeue: remove head
4. enquequ: add 
5. peek: look at head

6. 2 special type
- deque: double-ended queue, go both ways
- priority queue: assign numerical priority, get dequeued first


## Search
### Binary search
1. sorted array: for binary search, elements need to be in increasing order
2. from start/end: O(n)
3. from middle and choose left/right half

4. efficiency: O(log(N))


### Recursion
1. a function calls itself
2. a base case: while(exit condition)
3. alter the input for each iteration

## sort
1. memorize complexity
2. in place? => in original data stucture

### Bubble sort 
1. naive approach
2. compare side by side and switch when necessary
3. O(n-1)(n-1)=O(n^2)
4. best case O(n): 0 or 1 number needs to be bubbled
5. in place, space complecity: O(1)


### Merge sort
1. split a huge down as much as possible and overtime, building it up
2. Principle -- divide and conquer
3. O(n * m),m=log(n)
4. capture the intervals where the change happens
5. bad auxillary space=O(n)


### quick sort
1. pivot: last element by convention
2. find the right position for the pivot ()
3. recursively picking pivot 
4. worst: O(n^n) -- pivot is the largest, best O(n ^ logN) -- pivot should be the middle
5. in place
6. improvement: find the median among last few elements


## Map
1. key-value structure
2. look up sth by its name and go some location to get the value

### Set
1. no order, no repetition

2. Map is Set based data structure, Array is List based structure

3. the group of keys in a map are a set: unique


## Hashing
1. use a data structure that employs a hash function allows you to do look-ups in constant time
2. linear time search for other data structure
* List, set: look through every element to find the one you are looking for
* stacks and queues let you to look up the oldest/newest element immediately
* priority queues let you find the highest priority element quickly

3. value -------> hash value

4. last few digits -> reminder(hash code) -> save in an array(hash code as the index) -> look up by index (const time)

5. collision
* change hash function
* change structure of the array: save a list hashed in one spot -- bucket


### Hash Maps
1. hashing the key and save <key,value> in one buckets produced by the hash function



## Tree
1. An extension of linked list
2. constaints: 
* completely connected
* no cycle
3. term
* nodes: individual elements that contain values
* level
* parent-child relationship, ancestor-descendant
* leaves, external node
* height of node: leave node(0)
* height of tree: height of root node
* depth: number of edges to the root


### tree traversal
1. DFS
2. BFS: level order
#### Depth-First Traversals
1. pre-order
2. in-order
3. post-order

#### Search and Delete
1. search: O(n)
2. delete: O(n)


#### Insert
1. traverl through of the number of node that equals to the height of the tree

2. height of a binary tree
* level=log(n)

#### Binary Tree
1. each node can have most 2 children

## Some common tree types
1. what tasks were they speed up
2. what cons and pros

#### Binary Search Tree (BST)
1. a type of Binary Tree
2. Rule:
* every value on the left of a particular node is smaller than it 
* do search, insertion and delete quickly
3. search: run time is the height of the tree: O(logN)
4. complications: unbalanced binary tree, worst case for BST, O(n), just a linked list

#### Heap
1. another specific type of tree,complete tree,left first, elements are arranged in increasing or decreasing order
2. max heaps: root is the biggest; min heaps: root is smallest
3. max heap
* function get the maximum value: peek(), O(1)
* search: O(n), averageO(n/2)
* insert: heapify, O(logN) --> height of the tree
4. implementation: usually as arrays
* save the pointers than saving it as tree node object

#### Self-Balancing Tree
1. try to minimize the number of levels it uses

#### Red-Black Tree
1. rule 1: nodes are assigned additional color property: red or black
2. rule 2: second property: existence of null leaf nodes -- black
3. rule 3: both children of a red node should be black
4. rule 4 (optional): root node -- black
5. rule 5: every path from the node to the null leave must contain the same number of black nodes


6. insertion

#### Tree Rotation


## Graph (network)
1. graph is a data structure designed to shwo relationships between object
2. node - vertex, edge, can both save data, depends on what I use this graph for
3. tree is a more specific type of graph
4. forms a cycle, no root



### Direction and cycles
1. directed graph: has edges with direction
2. undirected graph
3. cycles can be very dangerous: infinite loop -- acyclic
4. DAG: directed, acyclic graph

### connectivity
1. the minimum number of elements that needs to be removed for a graph to become disconnected


### representation
1. Object: vertx object / edge object -- search is hard
2. Edge List: `[[0,1],[1,2],[1,3][2,3]]` --> two nodes has edge between them

2D-list

3. Adjacency list: `[[1],[0,2,3],[1,3][2,1]]`: ID of a node is index of the array, the value is the nodes that is adjacent to the node

### Adjacency Matrix -- rectangle array
```
[
[0,1,0,0]
[1,0,1,1]
[0,1,0,1]
[0,1,1,0]
]
````

### Grapgh traversal
1. no obvious node to start


### depth-first search --O(2E+V)
1. seen
2. add to the stack
3. pick an edge, add to stack 
4. see the seen, go previous node, try other edges
5. pop off the nodes with all visited edge

6. or use recursion

### breadth-first search -- --O(2E+V)
1. seen
2. visit all adjacent node
3. add to queue
4. dequeue

5. like building a tree


### notable paths 
1. eulerian pat:h start at one node, traverse through all edges, and end at one node

2. hamiltonian path: traverse all nodes
