### Description
A `std::unique_ptr` is a smart pointer for exclusive ownership. Meaning only one `unique_ptr` is allowed to own an object at a time. When it leaves scope, it automatically deletes the object it owns.

### Examples
```c++
#include <memory>

void myFunction() {
	std::unique_ptr<int> p = std::make_unique<int>(10);
	// Can use *p to dereference value

	std::unique_ptr<int> p2 = std::move(p);  // Now owned by p2, p is nullptr
	// Can use *p2 to dereference value
} // p2 leaves scope and memory is cleaned up
```

### See Also
* [[Smart pointers]]
* [[Shared Pointers]]
* [[Weak Pointers]]