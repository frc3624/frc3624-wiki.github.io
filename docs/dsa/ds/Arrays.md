# Arrays


## Theory
### What is it?
#### **Static Arrays**
A static array is a fixed length container containing n elements indexable from the range [0, n-1]
NOTE: Indexable means that each index of the array can be referenced with a number

Alongside this, static arrays take up a contiguous chunk of memory for the computer
#### **Dynamic Arrays**
Arrays which can grow and shrink in size as needed 

<br>

### When is it used?
#### **Static Arrays**
- Storing and accessing sequential data
- Temporarily storing objects
- Used by IO routines as buffers
- Lookup tables and inverse lookup tables
- Can be used to return multiple values from a function
- Used in dynamic programming to cache answers to subproblems

<br>

### Complexity
| Operation | Static | Dynamic |
|---------- | ------ |-------- |
| Access    | O(1)   | O(1)    |
| Search    | O(n)   | O(n)    |
| Insertion | N/A    | O(n)    |
| Appending | N/A    | O(1)    |
| Deletion  | N/A    | O(n)    |


## Usage Example
### Dynamic Array Implementation
1) Create a static array with an initial capacity
2) Add elements to the underlying static array, keeping track of the number of elements
3) If adding another element will exceed the capacity, then create a new static array with twice the capacity and copy the original elements into it

<br>


## Code
This is more or less how the built in Array class works. I won't touch on this too much because there's not much purpose.
### Add Method
This add method adds a new element to the dynamic array by implementing static arrays. This method doubles the size of the current array in order to add another element if the current size is too small.  
```java
public void add(T elem) {
    if (len+1 >= capacity) {
        capacity = capacity == 0 ? 1 : capacity # 2;
        T[] new_arr = (T[]) new Object[capacity];
        for(int i = 0; i < len; i++) {
            new_arr[i] = arr[i];
        }
        arr = new_arr
    }
}
```

### Remove Method
Similar algorithm, creates a new array which is one smaller. Then copies up to the index, skips the index, and copies the remainder
```java
public T removeAt(int rm_index) {
    if(rm_index >= len && rm_index < 0) throw new IndexOutOfBoundsException();
        T data = arr[rm_index];
        T[] new_arr = (T[]) new Object[len-1];
        for(int i = 0, j = 0; i < len; i++, j++) {
            if(i == rm_index) j--;
            else new_arr[j] = arr[i]
        }
        arr = new_arr;
        capacity = --len;
        return data;
}
```
