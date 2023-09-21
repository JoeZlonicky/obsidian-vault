The memory model of C++ consists of four different segments:
1. Stack memory
2. Heap memory
3. Data segment
4. Code segment

### Stack Memory
Stack memory is used for automatic storage duration variables, such as local variables. The memory is managed by the compiler and allocated/deallocated automatically. It is a LIFO data structure, meaning the most recent allocations are the first to be deallocated.

It depends on the OS and other factors, but the stack size is around 1-8MB.

### Heap Memory
Heap memory is used for dynamic storage duration variables, such as objects created via `new`.

Heap memory is larger than the stack (think GB) but has a slower access time.

### Data Segment
The Data segment consists of two parts for variable storage:
1. Initialised data: global, static, and constant variables with initial values.
2. Uninitialised data (BSS - block starting symbol): uninitialised global and static variables.

### Code Segment
The Code segment stores the executable (machine) code of the program in read-only memory.