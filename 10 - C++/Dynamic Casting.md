### Definition
`dynamic_cast` is a casting method specifically for casting to derived polymorphic classes. If the cast fails then a `nullptr` will be returned, making it easy to confirm if the cast was successful.

For a class to be polymorphic and thus valid for dynamic casting, the base class must have at least one virtual method.

### Examples
```cpp
#include <iostream>

class Base {
    virtual void myFunction() {
        std::cout << "Base" << std::endl;
    }
};

class Derived {
    void myFunction() override {
        std::cout << "Derived" << std::endl;
    }

    void secondFunction() {
        std::cout << "Second function" << std::endl;
    }
};

int main() {
    Base* myObj = new Derived();
    Derived* casted = dynamic_cast<Derived*>(myObj);
    if (casted != nullptr) {
        // Know myObj is a valid Derived instance
        casted->secondFunction();  // Safe to call!
    }

    delete myObj;
    return 0;
}
```
