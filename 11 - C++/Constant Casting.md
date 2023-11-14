### Description
`const_cast` is a method to be used on pointers/references to add/remove a constant or volatile modifier.

Note that it should not be used to modify a constant object, as that would be undefined behavior, but it should rather be used to change non-constant objects referenced via a constant access path, or to satisfy function parameter type when safe to do so.

This is most helpful when you are working with external code that you are unable to modify.
### Examples
```cpp
#include <iostream>

// pretend this is some external function 
void myFunction(int* p) {
    std::cout << *p << std::endl;
}

int main() {
    const int a = 10;
    const int* myPointer = &a;

    // myFunction won't accept myPointer!

    int* secondPointer = const_cast<int*>(myPointer);

    // Changing value now would be undefined behavior

    myFunction(secondPointer);  // Works!

    return 0;
}
```

```cpp
#include <iostream>

int main() {
    int a = 10;
    const int& b = a;

    // Can't change via b even though a isn't const
    
    int a2 = const_cast<int>(b);
    a2 = 5;  // can change again!

    return 0;
}
```