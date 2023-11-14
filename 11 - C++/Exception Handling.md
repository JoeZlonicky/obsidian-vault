### Description
Exception handling is a method to tackle runtime errors so that normal flow of the program can be maintained. In C++ this is accomplished using
1. `try`
2. `catch`
3. `throw`

The STL provides a standard set of exception classes that can be used directly or inherited, including
1. `std::exception`: base class for all standard exceptions
2. `std::invalid_argument`: for invalid arguments being passed in
3. `std::out_of_range`: commonly used for an invalid index while accessing a container
### Examples
```c++
int main() {
	try {
		// Something went wrong!
		throw 20;
	}
	catch (int e /* = 20 */) {
		// Handle exception
	}
}
```

```c++
#include<stdexcept>

void myFunction(int x) {
	if (x == 0) {
		throw std::runtime_error("x can not be zero!");
	}
}

int main() {
	try {
		myFunction(0);
	} catch (const std::exception& e) {
		// Handle error
	}
	
	return 0;
}
```

### See Also
* [[Noexcept]]