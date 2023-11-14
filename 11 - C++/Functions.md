### Description
Syntax: `returnType functionName(...parameters...) {}`
A return type of `void` means nothing is returned.
### Examples
```run-cpp
#include <iostream>

void printHello() {
	std::cout << "Hello!" << std::endl;
}

void printSum(int a, int b) {
	std::cout << a + b << std::endl;
}

int main() {
	printHello();
	printSum(5, 5);
	
	return 0;
}
```

### More Details
If no parameters are needed then either no parameters can be specified, or the keyword `void` can be used.

### See more
* [[Forward Declaration]]
* [[Lambda Functions]]
* [[Function Pointers]]
* [[Noexcept]]
* [[Function Overloading]]