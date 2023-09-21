### Description
Exit codes are numeric values that a program returns when it finishes execution. Usually 0 means success and anything else means failure. You can return an exit code from the main function, or by using the `std::exit()` function of the STL.

### Examples
```c++
void myFunction() {
	// Some error has happened!
	std::exit(1);  // 1 indicates failure
}

int main() {
	myFunction();
	
	// Some other code 
	
	return 0;
}
```