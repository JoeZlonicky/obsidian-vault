Functors are a class or a struct object that can be called like a function. This is achieved by overloading the functional-call operator. The big advantage of this is that the function can maintain a state between calls.
```c++
class Ticker {
public:
	int count = 0;
	
	int operator()() {
		++count;
	}
}

Ticker myTicker;
myTicker(); // Now count = 1
myTicker(); // Now count = 2
```