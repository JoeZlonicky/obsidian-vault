### Description
Below are all of the bitwise operators.

|Operator|Usage|Notes|
|-|-|-|
|&|`int result = 5 & 3;  // = 1`|Performs a bitwise AND operation.|
|\||`int result = 5 │ 3; // = 7`|Performs a bitwise OR operation.|
|^|`int result = 5 ^ 3;  // = 6`|Performs a bitwise XOR operation.|
|~|`int result = ~5;  // result depends on int size`|Performs a bitwise NOT operation.|
|<<|`int result = 5 << 1;  // = 10`|Performs a bitwise left shift.|
|>>|`int result = 10 >> 1;  // = 5`|Performs a bitwise right shift.|

### Examples
```run-cpp
#include<iostream>

int main() {
	int x = 5;
	x = x | 9;  // 0101 | 1001 = 1101 = 13
	x = x << 1;  // 1101 << 1 = 11010 = 26
	
	std::cout << x << std::endl;
	return 0;
}
```
