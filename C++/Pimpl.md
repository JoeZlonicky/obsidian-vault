### Description
Pimpl (Pointer-to-implementation) is a technique for hiding the implementation details of a class by using a forward declaration to a private structure/class. This keeps the public interface clean and reduces compile-time dependencies.

### Examples
`MyClass.h`
```c++
class MyClassImplementation;

class MyClass
{
public:
	MyClass();
	~MyClass();
	void someMethod();

private:
	MyClassImplementation* pimpl;
};
```

`MyClass.cpp`
```c++
#include "MyClass.h"

class MyClassImplementation
{
public:
	void someMethod()
	{
		// Some messy method
	}
	// Can be as messy as it wants without polluting public interface
	// Can include dependencies in this source file instead of in header
};

MyClass::MyClass() : pimp(new MyClassImplementation()) {}

MyClass::~MyClass() {delete pimpl;}

void MyClass::someMethod()
{
	pimpl->someMethod();  // Nice and clean!
}
```