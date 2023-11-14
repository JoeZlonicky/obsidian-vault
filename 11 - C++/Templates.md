Templates allow for generic code that can work with different data types.

Both classes and functions can utilize templates.

### Examples
```cpp
#include <iostream>

template <typename T>
T add(T a, T b) {
    return a + b;
}

template <typename T>
class MyContainer {
public:
    MyContainer(T startValue) : value(startValue) {}
    void display() {
        std::cout << value << std::endl;
    }
    T getValue() {
        return value;
    }
private:
    T value;
};

int main() {
    int myValue = add<int>(2, 2);
    std::cout << myValue << std::endl;
    
    MyContainer<int> c {10};
    c.display();
    int value = c.getValue();
    
    return 0;
}
```