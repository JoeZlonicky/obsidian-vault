### Description
Virtual tables (often shortened to just v-tables) are a mechanism to support dynamic polymorphism. The table contains functions pointers to the correct implementation of the virtual methods. Each object with virtual methods has a pointer for its virtual table which is automatically initialised during compilation.

```run-cpp
#include <iostream>

class Base {
public:
	virtual void functionOne() {
		std::cout << "Base functionOne()" << std::endl;
	}
	
	void functionTwo() {
		std:: cout << "Base functionTwo()" << std::endl;
	}
};

class Derived : public Base {
public:
	void functionOne() override {
		std::cout << "Derived functionOne()" << std::endl;
	}
	
	void functionTwo() {
		std::cout << "Dervied functionTwo()" << std::endl;
	}
};


int main() {
	Base b;
	std::cout << "An instance of Base will call Base methods" << std::endl;
	b.functionOne();
	b.functionTwo();
	
	Derived d;
	std::cout << "\nAn instance of Derived will call Derived methods" << std::endl;
	d.functionOne();
	d.functionTwo();
	
	Base* bPointer = new Derived();
	std::cout << "\nNow that we just have a pointer it matters that we declared the method virtual!" << std::endl;
	bPointer->functionOne();
	bPointer->functionTwo();
	
	return 0;
}

```

### See Also
* [[Virtual methods]]