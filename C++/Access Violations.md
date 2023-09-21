### Description
Access violations are errors that occur when a program attempts to access an illegal memory location. The most common causes are from
1. Dereferencing a null or invalid pointer
2. Accessing an array out of bounds
3. Reading or writing to memory that has been freed (by user or OS)

### Examples
```run-cpp
int main() {
	int *p = nullptr;
	int x = *p;  // Access violation! p is a nullptr

	int arr[3] = {1, 2, 3};
	int y = arr[5];  // Access violation! 5 is out of bounds

	int* p2 = new int[10];
	delete[] p2;
	p2[6] = 9;  // Access violation! Memory has been freed already
	
	return 0;
}
```


