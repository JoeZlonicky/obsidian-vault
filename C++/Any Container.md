### Description
`std::any` is a container for a single value of any type. To access that value you can cast it to the stored data type.
### Examples
```run-cpp
#include<any>
#include<string>
#include<iostream>

int main() {
	std::any value;
	value = 42;
	std::cout << std::any_cast<int>(value) << std::endl;
	
	value = 3.14;
	std::cout << std::any_cast<double>(value) << std::endl;
	
	value = true;
	std::cout << std::any_cast<bool>(value) << std::endl;
	
	value = std::string("Hello, world!");
	std::cout << std::any_cast<std::string>(value) << std::endl;
	
	return 0;
}
```

### More Details
Like [[Void pointers]], `std::any` is prone to errors and can affect runtime performance. Should probably be avoided in production code. [[Templates]] can usually be used instead.

### See Also
* [[Dynamic Typing]]

