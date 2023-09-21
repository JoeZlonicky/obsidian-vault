### Description
Anonymous [[Namespaces]] allows you to write functions that can only be accessed from the file they are defined in.

### Examples
```run-cpp
#include<iostream>

namespace {
	void myFunction() {  // Can only be accessed in this file
		std::cout << "Hello, world!" << std::endl;
	};
}

int main() {
	myFunction();  // No namespace prefix
	return 0;
}
```