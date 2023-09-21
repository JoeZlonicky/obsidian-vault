Namespaces avoid name clashes and make code more modular.
```c++
namespace MyNamespace {
	int myFunction() {
		// ...
	}
	// ... More namespace functions
}

int main() {
	MyNamespace::myFunction();
	return 0;
}
```

### Using
The `using` keyword allows you to "import" namespace elements into the current scope.
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

Inclusions like `using namespace std;` are considered bad practice because it can lead to name conflicts and also make it confusing where something is coming from.

### Anonymous Namespaces
An anonymous namespace allows you to write functions that can only be accessed from the file they are defined in.
```c++
namespace {
	int myFunction() {  // Can only be accessed in this file
		// ...
	}
}

int main() {
	myFunction();  // No namespace prefix
}
```