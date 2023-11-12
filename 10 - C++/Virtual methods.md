### Description
Declaring a method as virtual tells the compiler that a method is expected to be overridden in a derived class. 

The `override` keyword is how the compiler is told this from the perspective of the derived class. If you have one and not the other then the compiler will throw an error. If you exclude both, then a pointer of the base type will fail to call the method of the derived class.

### Examples

```c++
class Vehicle {
public:
	virtual void drive() {
		// Default drive behavior
	}
};

class Car {
	void drive() override {
		// Override drive behavior for car stuff
	}
};

class Truck {
	void drive override {
		// Override drive behavior for truck stuff
	}
};

int main() {
	// Note that we need to use pointers if we want to allow for any of the derived class
	// Storing in a Vehicle variable would result in object slicing
	Vehicle* garage[2] = {new Car, new Truck};
	garage[0]->drive();  // Calls Car drive method
	garage[1]->drive();  // Calls Truck drive method
	
	delete garage[0];
	delete garage[1];
	return 0;
}
```

### More Details
Under the hood, having a virtual method results in the creation of [[Virtual Tables]].