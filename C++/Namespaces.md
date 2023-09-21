### Description
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

### See Also
* [[Using Keyword]]
* [[Anonymous Namespaces]]