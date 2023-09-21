### Description
Utilising smart pointers has various advantages over raw pointers:
1. Prevent dangling pointers (point to memory that has been deleted)
2. Reduce memory leaks (memory that is never deleted)
3. Don't have to handle manual memory management (i.e. deal with problems 1 and 2)

While still offering all of the benefits of allocating on the heap:
1. Dynamically sized memory allocation
2. Large memory space (compared to stack)

### More Details
There are three types of smart pointers provided by the C++ STL:
1. [[Unique Pointers]]
2. [[Shared Pointers]]
3. [[Weak Pointers]]
