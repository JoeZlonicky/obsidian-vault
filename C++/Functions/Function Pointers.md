Pointers can also store the memory address of a function. They can be specified with the format of `returnType (*pointerName) (...parameterTypes...)`

```c++
int add(int a, int b) {
	return a + b;
}

int main() {
	int (*func) (int, int) = add;
	int result = func(4, 5);
}
```