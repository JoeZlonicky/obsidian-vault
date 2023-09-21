In C++ there are four types of scope:
1. Global scope
2. Local scope
3. Class scope
4. Namespace scope

### Global Scope
Identifiers declared outside any function, namespace, or class, have global scope. They can be accessed from any part of the program and their lifetime is the entire duration of the program ([[Object Lifetime]]).

### Local Scope
Identifiers declared inside a function or block have local scope and can only be accessed within the corresponding function/block.
```c++
void myFunction() {
	int myVar = 2;
	{
		int secondVar = 3;
	}  // secondVar leaves scope
}  // myVar leaves scope
```

### Namespace Scope
See [[Namespaces]].

### Class Scope
Identifiers declared within a class have class scope and can be accessed by
1. The `::` operator (if a static member)
2. The `.` operator (if a non-static member)
3. The `->` operator (through a pointer to a non-static member)
```c++
class MyClass {
public:
	static int staticMember;
	int nonStaticMember;
	
	MyClass(int value) : nonStaticMember(value) {}
};

int main() {
	MyClass::staticMember = 7;
	
	MyClass obj{10};
	obj.nonStaticMember = 2;
	
	MyClass* p = &obj;
	p->nonStaticMember = 3;
	
	return 0;
}
```