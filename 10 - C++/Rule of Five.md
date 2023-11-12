### Description
The Rule of Fives goes two steps further and suggests including two additional special member functions to allow for greater optimisation:
1. Move constructor
2. Move assignment operator

### Examples
```c++
	// Rest of class...
	
	// Noexcept is a compiler optimization for move constructors/assignments
	// Some containers like vectors may only use move if function is noexcept
	MyResourceHandler(MyResourceHandler&& other) noexcept : data(other.data) {
		other.data = nullptr;
	}
	
	MyResourceHandler& operator=(MyResourceHandler&& other) noexcept {
		if (&other == this) { return *this; }
		delete[] data;
		data = other.data;
		other.data = nullptr;
		return *this; 
	}

```

### See Also
* [[Rule of Zero]]
* [[Rule of Three]]