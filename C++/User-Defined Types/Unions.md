Unions are used to store different data types in the same memory location. 
```c++
union Data {
	int num;
	char letter;
	float decimal;
};

int main() {
	Data myData;
	myData.num = 42;
	myData.letter = 'a';  // No longer storing 42
	return 0;
}
```

Unions are usually stored inside of [[Classes]] or [[Structures]] so the type of data being stored can be tracked.