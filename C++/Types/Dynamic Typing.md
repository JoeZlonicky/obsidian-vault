Although C++ is known for [[Static Typing]], there are some mechanisms for achieving a certain level of dynamic typing:
1. `void*` pointers
2. `std::any`

### void* pointers
A `void*` pointer is a generic pointer that can point to an object of any data type. It must be cast to another type to dereference the value.
```c++
int main() {
	int x = 42;
	float y = 3.14f;

	void* genericPointer = &x;
	int someInteger = *(static_cast<int*>(genericPointer));

	genericPointer = &y;
	float someFloat = *(static_cast<float*>(genericPointer));
	
	return 0;
}
```

### std::any
`std::any` is a container for a single value of any type.
```c++
#include <any>

int main() {
	std::any value;
	value = 42;
	value = 3.14;
	value = true;
	
	return 0;
}
```