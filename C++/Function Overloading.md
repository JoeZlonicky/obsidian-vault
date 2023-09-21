### Description
Function overloading allows you to use the same function name for different parameter lists. The appropriate function to call is determined during compile-time.

### Examples
```run-cpp
#include <iostream>

void myFunction(int x) {
	std::cout << "I was called with an integer!" << std::endl;
}

void myFunction(float x, float y) {
	std::cout << "I was called with two floats!" << std::endl;
}

void myFunction(std::string s) {
	std::cout << "I was called with a string!" << std::endl;
}

int main() {
	myFunction(2);  // Calls int function
	myFunction(2.4f, 1.9f);  // Calls float function
	myFunction("Hello");  // Calls string function
	
	return 0;
}
```