### Description
Functors are a class or a struct object that can be called like a function. This is achieved by overloading the functional-call operator. The big advantage of this is that the function can maintain a state between calls.

### Examples
```run-cpp
#include <iostream>

class Ticker {
public:
	int count = 0;
	
	void operator()() {
		++count;
	}

	void display() {
		std::cout << count << std::endl;
	}
};

int main() {
	Ticker myTicker;
	myTicker(); // Now count = 1
	myTicker(); // Now count = 2

	myTicker.display();
	
	return 0;
}


```