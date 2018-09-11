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

