### Description
The Rule of Three states that a class/structure that manages resources should define all three of these special member functions:
1. Destructor
2. Copy constructor
3. Copy assignment operator

### Examples
```c++
class MyResourceHandler {
public:
	MyResourceHandler() : data(new int[100]) {}

	~MyResourceHandler() { delete[] data; } // 1 - Destructor

	// 2 - Copy constructor
	MyResourceHandler(const MyResourceHandler& other) : data(new int[100]) {
		std::copy(other.data, other.data + 100, data);
	}

	// 3 - Copy assignment operator
	MyResourceHandler& operator=(const MyResourceHandler& other) {
		if (&other == this) { return *this; }  // Handle self-assignment
		std::copy(other.data, other.data + 100, data);
		return *this;
	}
private:
	int* data;
}
```

### See Also
* [[Rule of Zero]]
* [[Rule of Five]]