### Description
Forward declaration is a way to declare symbols (class, function, or a variable) before defining it in code. This is particularly useful for avoiding cyclic dependencies, as well as reducing compilation time by not including unnecessary header files.

### Examples
```run-cpp
#include<iostream>

class MyClass;  // Can be used for parameter types and the like

void myFunction(MyClass& obj);  // MyClass would need to be defined before function is defined

int calculateSum(int a, int b);  // Declare function here

int main() {
	int sum = calculateSum(2, 3);
	std::cout << "The sum is: " << sum << std::endl;
	return 0;
}

int calculateSum(int a, int b) {  // Define it down here
	return a + b;
}
```
### More Details
When forward declaring classes, if you try to make an object of the declared class or call its member functions without defining the class, there will be a compilation error. Thus this is the most helpful in header files of classes where you usually just need the class name for parameter lists.

It is not possible to forward declare an `enum` or `typedef` because they don't have separate declaration and definition stages.