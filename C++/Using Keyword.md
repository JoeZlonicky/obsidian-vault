### Description
The `using` keyword allows you to "import" namespace elements into the current scope.

### Examples
```c++
namespace MyNamespace {
	int myFunction() {
		// ...
	}
	// ... More namespace functions
}

int main() {
	using MyNamespace::MyFunction;  // Import specific element
	// using MyNamespace;  // Imports entire namespace
	myFunction();
	return 0;
}
```

### More Details
Inclusions like `using namespace std;` are considered bad practice because it can lead to name conflicts and also make it confusing where something is coming from.