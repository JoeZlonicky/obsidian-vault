References share the memory location of another variable, creating an alias.
```c++
int num = 42;
int& numReference = num;
++numReference;  // num and numReference are now both 43
```
Unlike [[Pointers]], references cannot be reassigned and cannot "point" to nothing. If you want either of these features you should use a pointer instead.

References are most often used when wanting to pass a variable by reference into a function, either to avoid copying the value or to be able to change it within the scope of the function.
```c++
// Since num is passed by reference, changes will persist after function call
int addOne(int& num) {++num;}
```