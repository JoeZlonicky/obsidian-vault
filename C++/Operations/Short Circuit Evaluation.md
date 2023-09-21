In C++, if the left operand of an OR or AND operation is true or false, respectively, then the right operand will not be evaluated. This saves performance and is also very handy when you want conditional evaluation of the right operand.
```c++
int main() {
	SomeClass* myPointer = nullptr;
	if (myPointer && myPointer->function()) {
		// Will not call function if myPointer is a null pointer
		// This is good because otherwise it would crash!
	}

	int x = 0;
	if (x == 0 || someExpensiveFunction()) {
		// The expensive function will only be called if needed!
	}
}
```