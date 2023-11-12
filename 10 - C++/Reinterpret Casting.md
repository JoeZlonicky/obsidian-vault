`reinterpret_cast` is a casting method for changing the type of a pointer without altering the representation of the data itself.

### Examples
```cpp
#include <iostream>

int main() {
    int num = 342;
    int* intPointer = &num;
    char* cPointer = reinterpret_cast<char*>(intPointer);

    for (int i = 0; i < sizeof(int); ++i) {
        std::cout << cPointer[i] << std::endl;
    }
    return 0;
}
```