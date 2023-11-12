### Description
Arrays are used to store multiple values of the same type in consecutive memory locations.

### Examples
```run-cpp
#include<iostream>

int main() {
	int numbers[5] = {1, 2, 3, 4, 5};
	for (int i = 0; i < 5; ++i) {
		std::cout << numbers[i] << '\n';
	}
	std::flush(std::cout);
	
	return 0;
}

```


