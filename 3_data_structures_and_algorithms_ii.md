# Sprint 3: Data Structures and Algorithms II

## Linked Lists
Time complexity for singly linked lists: 
* Insert or delete at beginning: O(1)
* Access a specific index: O(n) (we have to traverse node by node to get to the desired index)
* Insert or delete at a specific index: O(n) 

Variations:
* Singly Linked List (the standard version, each node stores a value and next pointer)
* Doubly Linked List (each node stores a value and both next and previous pointers)
* Circular Linked List (last node points to the first node rather than None)

In a singly-linked list, you may only traverse forward using the "next node" pointers, while in other implementations you may also be able to traverse backwards or go around the horn from end to beginning.

Depending on the implementation, you'll generally always have access to the "head" node (beginning of list) and also the "tail node" (end of list) in the case of a doubly linked list. 

Algorithms problems involving linked lists are often testing your ability to manipulate pointers, traverse through a linked list and handle edge cases. Here are some tricks that are helpful for many common whiteboarding questions:
* Dummy head: Create a dummy starting node and construct a list using its next pointer. Useful for handling edge cases like traversing an empty list
* Two-pointer technique: use two pointers to manipulate references to nodes. Useful for getting info about a list, e.g., detecting a cycle


## Queues and Stacks
A queue is a data structure that stores its items in a first-in, first-out (FIFO) order. 
A stack data structure handles information in a last-in, first-out (LIFO) order.

The names are helpful in remembering exactly these work! A queue is just like people standing in line, while a stack functions like a stack of plates. 

### Implementing a Queue
Elements can be added only at one end, the "rear", Elements can be removed only at the other end, the "front".
We call adding to a queue "enqueueing", and removing from a queue "dequeueing".

Use a linked list or dynamic array to implmement a queue.

### Implementing a Stack
Elements can be added to or removed from a stack at only one end. Since we view this end as the "top" of the stack, we use the term "push" for add, and the term "pop" for remove. 

Use a linked list or dynamic array to implement a stack.

# Binary Search Trees

## Tree Traversal

## Additional Resources
* [Data Structures: Linked Lists](https://www.youtube.com/watch?v=njTh_OwMljA&ab_channel=HackerRank)
