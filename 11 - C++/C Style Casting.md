### Definition
C-style casting is a casting syntax inherited from C.

[[Static Casting]] can be used instead and is generally better and safer.

### Examples
```cpp
#include <iostream>

int main() {
    int a = 10;
    float b = (float)a;  // C style cast
    std::cout << b << std::endl;
    
    return 0;
}
```