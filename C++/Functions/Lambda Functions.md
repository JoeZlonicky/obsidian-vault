Syntax: `[...captureList...](...parameters...) -> returnType {}`

For example:
```c++
	auto printHello = []() { /* print hello */ };
	printHello();
	
	auto add = [](int a, int b) -> int { return a + b; };
	int sum = add(1, 3);
	
	auto multiplyBySum = [sum](int multiplier) -> int {
		// sum is captured by value/copy
		return sum * multiplier; 
	};
	int product = multiplyBySum(3);

	auto updateSum = [&sum](int newValue) { 
		// sum is captured by reference
		sum = newValue;
	};
	updateSum(2);
```

**Note:** lambdas actually just generate the corresponding [[Functors]] with no extra overhead.
### Capturing
`[&]` captures the surrounding scope by reference.
`[=]` captures the surrounding scope by value/copy.
`[&, a]` captures the surrounding scope by reference except for `a` which it captures by value/copy.
`[=, &a]` captures the surrounding scope by value/copy except for `a` which it captures by reference.
`[this]` captures the current object by reference.
`[*this]` captures the current object by value/copy.

By default, values captured by value/copy are constant. To change this, append the `mutable` keyword to a lambda:
```c++
int x = 5;
auto xPlusOne = [x]() mutable -> int {
	++x;  // Allowed because mutable
	return 
};

int y = xPlusOne();
```