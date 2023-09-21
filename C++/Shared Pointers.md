### Description
A `std::shared_ptr` is a smart pointer that allows for shared ownership. A reference counter keeps track of how many shared pointers are in scope, and when it reaches 0 the memory will be cleaned up.

### Examples
```c++
#include <memory>

void myFunction() {
	std::shared_ptr<int> p = std::make_shared<int>(10);  // Ref count is 1
	// Can use *p to dereference value

	{  // Block scope
		std::shared_ptr<int> p2 = p;  // Ref count is incremented to 2
		// Can use *p or *p2 to dereference value
	}  // p2 leaves scope, ref count decrements to 1
	
	// Can still use *p to dereference value
}  // p leaves scope, ref count decrements to 0, memory is cleaned up

```

### More Details
For a non-owning reference (i.e. one that doesn't affect the ref count), see [[Weak Pointers]].