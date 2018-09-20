
# ADT - abstract data type

# list
1. one byte of memory has an address, one integer requires 4 bytes, 32 bits
2. programmer use programming language to talk to memory, address of the block of memory is the address of first byte
3. In C, array created using "malloc", we can use "realloc" to re-size it. Some memory block may be extended if space adjacent to the block is available.

# linked-list
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


# doubly linked-list
```
struct Node {
  int data;
  struct Node* next;
  struct Node* prev;
};
```

# stack
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

# queue
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
