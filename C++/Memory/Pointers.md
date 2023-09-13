Pointers are used to store the memory address of a variable.
```c++
int num = 42;
int* pointer = &num;  // Points to memory location of "num"

if (pointer != nullptr) {  // Dereferencing null pointer = undefined behavior
	// Asterisk dereferences pointers to give the value at the memory location
	std::cout << *num << std::endl;  
}

```

You can also have [[Function Pointers]]