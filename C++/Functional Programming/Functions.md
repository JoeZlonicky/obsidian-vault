Syntax: `returnType functionName(...parameters...) {}`

For example:
```c++
void printHello() {  /*print hello*/}
int calculateSum(int a, int b) {return a + b;}
```
A return type of `void` means nothing is returned.

If no parameters are needed then either no parameters can be specified, or the keyword `void` can be used.

Sometimes, either for organisation or for circular references, you want to declare a function and then define it later. To do this you declare a function prototype and then have the definition further down:
```c++
int calculateSum(int a, int b);

int main() {
	int sum = calculateSum(2, 3);
	return 0;
}

int calculateSum(int a, int b) {
	return a + b;
}
```

For defining anonymous functions, see [[Lambda Functions]].