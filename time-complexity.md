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
#### Depth-First Traversals


#### Search and Delete

#### Insert

#### Binary Search Tree

#### Heap

#### Self-Balancing Tree

#### Red-Black Tree


#### Tree Rotation
