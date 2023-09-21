Forward declaration is a way to declare symbols (class, function, or variable) before defining it in code. This is particularly useful for avoiding cyclic dependencies, as well as reducing compilation time by not including unnecessary header files.

Note that it is not possible to forward declare an `enum` or `typedef` because they don't have separate declaration and definition stages.
### Class Forward Declaration
```c++
class MyClass;  // Forward declaration

void myFunction(MyClass& obj);
```
However if you try to make an object of the declared class or call its member functions without defining the class, there will be a compilation error. Thus this is the most helpful in header files of classes where you usually just need the class name for parameter lists.

### Function Forward Declaration
For the sake of organisation or for avoiding circular references, you can define a function prototype and then define to further down in the file:
```c++
int calculateSum(int a, int b);

int main() {
	int sum = calculateSum(2, 3);
	return 0;
}

int calculateSum(int a, int b) {
	return a + b;
}
```