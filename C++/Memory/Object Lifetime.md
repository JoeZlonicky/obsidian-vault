In C++, object lifetime can be classified into four categories:
1. Static 
2. Thread
3. Automatic
4. Dynamic

See [[Memory Model]] for how these objects are stored.
### Static Storage Duration
Objects with static storage duration exist for the entire run of the program. They are allocated at the start of the program running and deallocated when the program terminates. Global variables, static data members, and static local variables all fall into this category.

### Thread Storage Duration
Objects with thread storage duration exist for the lifetime of the thread they belong to. They are created when a thread starts and destroyed when a thread exists. Thread storage duration can be specified via the `thread_local` keyword.
```c++
thread_local int myVar;
```

### Automatic Storage Duration
Objects with automatic storage duration are created at the point of definition and destroyed when the declaration scope is exited. Function parameters and local non-static variables fall into this category.
```c++
void myFunction() {
	int myVar = 2;  // Defined and created
}  // Destroyed
```

### Dynamic Storage Duration
Objects with dynamic storage duration are created at runtime using memory allocation functions (e.g. `new`). It is up to the programmer to destroy the objects (e.g. using `delete`).
```c++
int* ptr = new int;  // Created at runtime
// Exists until deleted
delete ptr;  // Deleted!
```