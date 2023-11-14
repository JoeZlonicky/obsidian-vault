### Description
Virtual inheritance guarantees that only one of a base class is inherited when [[The Diamond Problem]] occurs. This is implemented by adding the `virtual` keyword to inheritance.

### Examples
```Cpp
class Base {};

class Derived1 : virtual public Base {};
class Derived2 : virtual public Base {};

// only has one "Base" inherited because the classes inherited Base virtually
class MyClass : public Derived1, public Derived2 {};
```

### See Also
* 