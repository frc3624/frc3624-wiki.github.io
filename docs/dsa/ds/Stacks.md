# Stacks

## Theory
### What is it?
- One ended linear data structure which models a real world stack by having two primary operations, namely push and pop
- Follows LIFO (Last In First Out)
  
- Popping removes the top element, Pushing adds a new top element

<br>

### When is it used?
- Used by undo mechanisms in text editors
- Used in compiler syntax checking for matching brackets and braces
- Can be used to model a pile of books or plates
- Used behind the scenes to support recursion by keeping track of previous function calls
- Can be uused to do a Depth First Search (DFS) on a graph

<br>

### Complexity
| Operation | Stack |
|-----------|-------|
| Pushing   | O(1)  |
| Popping   | O(1)  |
| Peeking   | O(1)  |
| Searching | O(n)  |
| Size      | O(1)  |

### Usage Example
#### Brackets
Given a string made up for bracket sequences, determine whether the brackets properly match:

- Push each opening bracket [,{,( onto the stack
- When you encounter a closing bracket ],},):
  - First check that the stack is not empty
  - If the top is corresponding, then pop the corresponding bracket
  - If this is not the case, you have an invalid sequence

```python
from collections import dequeue
stack = dequeue()

for bracket in bracket_string:
    rev = getReversedBracket(bracket)
    if isLeftBracket(bracket):
        stack.push(bracket)
    elif len(stack) == 0 or s.pop() != rev:
        return false
return stack.isEmpty()

def isLeftBracket(bracket):
    return ['[','(','{'].contains(bracket)
def getReversedBracket(bracket):
    if bracket == '['
        return ']'
    if bracket == '{'
        return '}'
    if bracket == '('
        return ')'
```

## Implementation
Stacks are typically implemented as singly/doubly linked lists, but sometimes are also implemented using arrays
### Pushing on stack
In a linked list, the trick is to make the head of the LL become the newly pushed element
 
<br>

### Popping from stack
In a linked list, the trick is to set the next pointer of the head as the head, and set the old head to null so it is deallocated (garbage collector will take care of removal in Java, but manual deallocation is needed in C/C++)
## Code
