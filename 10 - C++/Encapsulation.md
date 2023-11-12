### Description
Encapsulation is about limiting external access to data or methods.

### Examples
```run-cpp
#include<iostream>

class Car {
public:
	Car() {}
	void drive(int distance) {
		milesTravelled += distance;
		std::cout << "I have now travelled " << milesTravelled << " miles!" << std::endl; 
	};
	
private:
	int milesTravelled = 0;
};

int main() {
	Car myCar;
	myCar.drive(100);
	// myCar.milesTravelled = -2;  // Can't do because private! Safe from myself.
	
	return 0;
}
```

### See Also
* [[Pimpl]]