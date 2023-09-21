### Description
Multiple inheritance is a C++ feature that allows you inherit from more than one parent class.

### Examples
```run-cpp
#include <iostream>

class Electric {
public:
	void charge() {
		std::cout << "Charging..." << std::endl;
	}
};

class Bike {
public:
	void peddle() {
		std::cout << "Off I go!" << std::endl;
	}
};

class ElectricBike : public Electric, public Bike { };

int main() {
	ElectricBike myBike;
	myBike.charge();
	myBike.peddle();
	
	return 0;
}
```
### See Also
* [[Diamond Inheritance Problem]]