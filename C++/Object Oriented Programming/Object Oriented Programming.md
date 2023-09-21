Object-oriented programming (OOP) is built on [[Classes]] and [[Structures]]. The core concepts of OOP are
1. Abstraction
2. Encapsulation: 
3. Inheritance
4. Polymorphism

### Abstraction
Abstraction is about hiding the details behind a concept.
```c++

class Car {
	void drive() {
		// Code...
	}
};

int main() {
	Car myCar;
	myCar.drive();  // I don't have to care about the details
}
```

### Encapsulation
Encapsulation is about limiting external access to data or methods.
```c++
class Car {
public:
	Car() : age(0) {}
	void drive(int distance) {
		milesTravelled += distance;
	};
	
private:
	int milesTravelled;
};

int main() {
	Car myCar;
	myCar.drive(100);
	// myCar.milesTravelled = -2;  // Can't do because private! Safe from myself.
}
```

### Inheritance
Inheritance is deriving new classes from existing ones. This improves code re-usability and organisation.
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

### Polymorphism
Polymorphism is about different classes inheriting the same interface.
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