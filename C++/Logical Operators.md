### Description
Below are all of the logical operators.

|Operator|Usage|Notes|
|-|-|-|
|&&|`if (a > 0 && b > 0)`|Performs an AND evaluation. If the left operand is false then the right won't be evaluated.|
|\|\||`if (a > 0 ││ b > 0)`|Performs an OR evaluation. If the left operand is true then the right won't be evaluated.|
|!|`if (!(a > 0))`|Performs a NOT evaluation.|
|\=\=|`if (a == b)`|Checks if operands are equal.|
|!=|`if (a != b)`|Checks if operands are not equal.|
|>|`if (a > b)`|Checks if left operand is strictly greater than the right|
|<|`if (a < b)`|Checks if left operand is strictly lesser than the right|
|>=|`if (a >= b)`|Checks if left operand is greater, or equal to, the right|
|<=|`if (a <= b)`|Checks if left operand is lesser, or equal to, the right|

### Examples
```c++
bool a = true;
a = !a;  // Will invert value

bool b = true;
if (a != b) {} // Does an XOR check
```

### More Details
Logical operations are always evaluated in the following priority:
1. !
2. &&
3. ||

Only the left operand may be evaluated in certain cases, due to [[Short Circuit Evaluation]].
