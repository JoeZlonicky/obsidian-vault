### Description
Pointers are used to store the memory address of a variable.

### Examples
```c++
int num = 42;
int* pointer = &num;  // Points to memory location of "num"

if (pointer != nullptr) {  // Dereferencing null pointer = undefined behavior
	// Asterisk dereferences pointers to give the value at the memory location
	std::cout << *num << std::endl;  
}

```

### More Details
Like [[References]] pointers can be used to pass objects around more efficiently. However pointers have the advantage of being null-able and to change what they point to.

See
* [[Function Pointers]]
* [[Smart Pointers]]