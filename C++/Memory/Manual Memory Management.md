Manual memory management can be used to dynamically allocate variables and arrays. Allocated objects are stored on the heap. See [[Memory Model]] for the advantages of this.

### new and delete
The `new` operator allocates memory on the heap. This memory will remain until explicitly deallocated with the `delete` operator. If you don't deallocate the memory, it will result in a memory leak.
```c++
int* ptr = new int;  // Allocates space for an integer on the heap
*ptr = 42;  // Assign a value
delete ptr;  // Clean up. Otherwise, memory leak!
```
### new[] and delete[]
The `new[]` and `delete[]` operators are very similar to the previous operators, but are specifically for working with arrays.
```c++
int n = 10;
int* array = new int[n];  // Allocated dynmically on the heap

for (int i = 0; i < n; ++i) {
	array[i] = i;
}

delete[] array;  // Clean up. Otherwise, memory leak!
```