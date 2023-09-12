There are two main mechanisms for RTTI in C++:
1. `typeid`
2. `dynamic_cast`
It's worth noting that both mechanisms result in additional information to be generated during compilation and stored and processed during runtime.
### typeid operator
`typeid` returns a reference to an object of type `std::type_info` which can be used to compare two types or to get specific information regarding the type.
```c++
#include <typeinfo>
#include <iostream>

class Base {};
class Derived : public Base {};

int main() {
	Base* instance = new Derived;
	std::cout << "Instance type: " << typeid(*instance).name() << std::endl;
}
```

### dynamic_cast operator
`dynamic_cast` can be used to either
1. Downcast a base pointer to a derived pointer (`nullptr` if cast fails).
2. Downcast a reference to a derived reference (`bad_cast` exception if fails).
```c++
class Base {};
class Derived : public Base {};

int main() {
	Base* instance = new Derived;
	Derived* castInstance = dynamic_cast<Derived*>(instance);
	if (castInstance != nullptr) {
		// Valid cast
	}
}
```

