The Rule of Zero, Three, and Five is a set of guidelines for managing object resources in modern c++.

### Rule of Zero
The Rule of Zero states that if a class or structure does not explicitly manage resources, it should not define any of the special member functions:
1. Destructor
2. Copy constructor
3. Copy assignment operator
Since the compiler will automatically generate these functions.

### Rule of Three
The Rule of Three states that a class/structure that manages resources should define all three of these special member functions:
1. Destructor
2. Copy constructor
3. Copy assignment operator

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

### Rule of Five
The Rule of Fives goes two steps further and suggests including two additional special member functions to allow for greater optimisation:
1. Move constructor
2. Move assignment operator

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