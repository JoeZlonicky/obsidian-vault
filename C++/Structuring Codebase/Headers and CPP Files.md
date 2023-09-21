Code splitting refers to the process of breaking down a large code base into smaller files or modules. This improves organisation, maintainability, and readability of the code. In C++, this is generally achieved through the use of header files, source files, and separate compilation.

### Header Files
Header files (`.h` or `.hpp`) are responsible for declaring classes, functions, and variables needed by multiple source files.
```c++
// MyHeader.h
#ifndef MY_HEADER_H
#define MY_HEADER_H

class MyClass {
public:
	myFunction();
};

#endif
```

Header files almost always have [[Include Guards]].
### Source Files
Source files (`.cpp`) are responsible for implementing the actual functionality defined in the corresponding header files.
```c++
// MyHeader.cpp
#include "MyHeader.h"  // Important

void MyClass::myFunction() {
	// Code
}
```

### Separate Compilation
C++ allows for separate compilation, which means that each source file can be compiled independently into an object file. Then the object files just need to be linked together to form an executable. This greatly improves compilation time when only a single source file was changed.
