### Description
|Control|Usage|Notes|
|-|-|-|
|if|`if (a > 5) {}`|Evaluates and then will execute code inside if true.|
|else|`if (a > 5) {}`<br>`else if (a < 0) {}`<br>`else {}`|Will execute statements if the previous if statement evaluated to false.|
|while|`while (a > 5) {}`|Executes statement inside as long as condition is true.|
|for|`for (int i = 0; i < 5; ++i) {}`|Initialises with first field, calls third field every iteration, and continues iteration until second field is false. Fields can be left empty.|
|for (ranged-based)|`for (char c : myString)`| Iterates a range. Requires the type being iterated to support this kind of iteration.|
|do-while|`do {} while(a > 5);`|Executes statements inside (always at least once) until the condition is false. Usually a normal while loop is used instead.|
|break|`while (a > 5) { break; }`|Breaks out of a loop. For nested loops it breaks out of the innermost loop.|
|continue|`while (a > 5) { continue; }` | Goes to next iteration of loop. The loop condition is still checked and for a for-loop the third field would still be executed.|
|goto|`label:`<br>`a++`<br>`goto label;`| Jumps to a label elsewhere in the code. Usually results in confusing/dangerous code. One useful case though is escaping multiple nested loops.|

### Examples
```run-cpp
#include<iostream>

int main() {
	int x = 3;
	if (x > 5) {
		std::cout << "X is greater than 5" << std::endl;
	} else if (x < 5) {
		std::cout << "X is less than 5" << std::endl;
	} else {
		std::cout << "X is exactly 5!" << std::endl;
	}

	while (x < 10) {
		++x;
		std::cout << "X is now: " << x << std::endl;
		if (x == 7) {
			std::cout << "Breaking out!" << std::endl;
			break;
		}
	}
}

```

### See Also
* [[Logical Operators]]

