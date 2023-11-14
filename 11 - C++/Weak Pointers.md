### Description
A `std::weak_ptr` is a smart pointer that is like a `std::shared_ptr` ([[Shared Pointers]]), but doesn't influence the reference count of an object. Before using it you have to lock the weak pointer as a shared pointer, which will only succeed if the object is still around. If it fails, you know the object has been freed. This mechanic is useful when you
1. Want to keep track of something, but don't want to keep it around if nothing else is using it.
2. Have two objects that point to each-other. This could result in a memory leak if they were both shared pointers.
3. Want something akin to a raw pointer ([[Manual Memory Management]]), but being able to check for a dangling pointer.

### Examples
```c++
#include <memory>

void myFunction() {
	std::weak_ptr<int> weak;
	
	{  // Block scope
		std::shared_ptr<int> shared = std::make_shared<int>(10);
		weak = shared;
		if (auto p = weak.lock()) {
			// If p is valid then weak points at something valid
			// Can dereference value via *p
		}
	}  // since weak doesn't increment ref count, memory is cleaned up
	
	if (auto p = weak.lock()) {
		// Won't occur because weak doesn't point to valid memory
	} else {
		// Handle this case
	}
}

```