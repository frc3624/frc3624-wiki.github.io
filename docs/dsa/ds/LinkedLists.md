# Linked Lists


## Theory
### What is it?
Sequential list of nodes that hold datwa which point to other nodes which also contain data
### When is it used?
- Used in many List, Queue, and Stack implementations
- Great for creating circular lists
- Can easily model real world objects such as trains
- Used in separate chaining, which is present in certain HashTable implementations to deal with hashing collisions
- Often used in the implementation of adjacency lists for graphs

<br>

### Terminology
- Head: The first node
- Tail: The last node
- Pointer: Reference to another node
- Node: An objects containing data and pointer(s)

<br>

### Complexity
| Operation        | Singly | Doubly |
|------------------|--------|--------|
| Search           | O(n)   | O(n)   |
| Insert at head   | O(1)   | O(1)   |
| Insert at tail   | O(1)   | O(1)   |
| Remove at head   | O(1)   | O(1)   |
| Remove at tail   | O(n)   | O(1)   |
| Remove in middle | O(n)   | O(n)   |

<br>

### Singly vs Doubly Linked
Singly linked lists have a pointer pointing towards the next node. This is more memory efficient as it only has pointer, however it's more taxing computationally if you want to delete a node just before another node because you need to search it O(n)

Doubly linked lists have a pointer pointing towards next node, as well the node prior. This takes twice the memory obviously, but it speeds up certain operations

## Implementation
### How to insert new elements
#### **Singly Linked**
- First make a node to the head
- Seek up to, but not including the node we want
- Create a new node, and make its next pointer to the existing node at the desired location
- Set the traversal node (the original node we had which advanced) to point to the new node
- This completes the insertion operation
#### **Doubly Linked**
- Once again, make a traversal node advance to the node we want
- Advance till we get to the node just before the desired, and create a new node
- Set this new node's back pointer to the traversal, and the forward to the node occupying the desired position
- Set the traversal's forward to the new node, and the node in the desired position's reverse to the new node
- This completes the insertion operation

<br>

### How to remove elements
#### **Singly Linked**
- We need to have 2 traversal nodes
- Advance both until you reach the desired node (with 1 node behind the other)
- Create a temp node for the desired node to delete, and advance the front traversal node ahead to the next node
- Set the back traversal node to point to the forward one
- Delete the temporary pointer from memory (set it to null)
- This completes the deletion operation
#### **Doubly Linked**
- Only 1 traversal node is required
- Advance to the desired node to delete from
- Set the desired's previous node to point to the traversal's forward
- Now set the desired's forward node to point towards the previous node as its reverse
- Now delete the node from memory (set it to null)
- This completes the deletion operation
## Doubly Linked List Code
