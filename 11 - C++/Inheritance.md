### Description
Inheritance is deriving new classes from existing ones. This improves code re-usability and organisation.

### Examples
```c++
class Car {
public:
	void drive() {
		// Code...
	}
};

// Need public specifier otherwise inherited methods will be private
class ElectricCar : public Car {
public:
	void charge() {
		// Code...
	}
};

int main() {
	ElectricCar myCar;
	myCar.drive();  // Inherited method
	myCar.charge();  // Specific to derived class
}
```

### See Also
* [[Multiple Inheritance]]
* [[Virtual methods]]
* [[Virtual Tables]]