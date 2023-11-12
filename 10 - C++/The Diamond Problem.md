### Description
The Diamond Problem occurs when a class inherits multiple classes which share a base class. It results in ambiguity due to having duplicate inherited classes.

The problem is solved by using [[Virtual Inheritance]].
### Examples
```cpp
#include <iostream>

class Base {
public:
    Base() {
        std::cout << "Base contructor" << std::endl;
    };
};

class Derived1 : public Base {
public:
    Base() {
        std::cout << "Contructor 1" << std::endl;
    };
};
class Derived2 : public Base {
public:
    Base() {
        std::cout << "Contructor 2" << std::endl;
    };
};

class MyClass : public Derived1, public Derived2 {};

int main() {
    // Uh oh! Base constructor will be called twice!
    MyClass myInstance;

    return 0;
}

```

### See Also
* [[Multiple Inheritance]]