### Description
A `void*` pointer is a generic pointer that can point to an object of any data type. It must be cast to another type to dereference the value.

### Examples
```c++
int main() {
	int x = 42;
	float y = 3.14f;

	void* genericPointer = &x;
	int someInteger = *(static_cast<int*>(genericPointer));

	genericPointer = &y;
	float someFloat = *(static_cast<float*>(genericPointer));
	
	return 0;
}
```

### See Also
* [[Pointers]]