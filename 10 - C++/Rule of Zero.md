### Description
The Rule of Zero states that if a class or structure does not explicitly manage resources, it should not define any of the special member functions:
1. Destructor
2. Copy constructor
3. Copy assignment operator
Since the compiler will automatically generate these functions.

### See Also
* [[Rule of Three]]
* [[Rule of Five]]