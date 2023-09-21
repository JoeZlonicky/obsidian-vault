Function overloading allows you to use the same function name for different parameter lists. The appropriate function to call is determined during compile-time.
```c++

void myFunction(int x) {
	// Handle an integer
}

void myFunction(float x, float y) {
	// Handle two floats
}

void myFunction(std::string s) {
	// Handle a string 
}

int main() {
	myFunction(2);  // Calls int function
	myFunction(2.4f, 1.9f);  // Calls float function
	myFunction("Hello");  // Calls string function
}
```